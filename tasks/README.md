# Pre-Test Bootcamp DevOps

## Task 1 (Virtualization)

Pada Pre-Test ini saya menggunakan tools IaC (Infrastructure as a Code) yaitu Terraform dan Ansible. Lalu saya juga menggunakan Google Cloud Provider (GCP) sebagai Server (VM) yang akan dibuat.

# Terraform

1. Melakukan setup arsitektur pada file providers.tf

```
terraform {
  required_providers {
    google = {
      source = "hashicorp/google"
      version = "6.7.0"
    }
  }
}

provider "google" {
  # Configuration options
  project = var.gcp_project_id
  credentials = var.credentials
  region = var.region
  zone = var.zone
}
```
![file-provider.tf](docs/terraform/terraform1.png)


1. Membuat file variable.tf yang digunakan untuk mendefinisikan seluruh variabel yang akan dipakai nantinya.

```
variable "region" {
  type = string
  description = "Region for TabelData Project"
  default = "asia-southeast2"
}

variable "zone" {
  type = string
  description = "Zone for TabelData Project"
  default = "asia-southeast2-a"
}

variable "images_OS" {
  type = map(map(string))
  description = "OS Images for Server"
}
```
![file-variable.tf](docs/terraform/terraform2.png)


3. Membuat file terraform.tfvars yang akan digunakan untuk mengatur nilai dari variabel yang sudah dibuat/didefinisikan pada file variable.tf.

```
 # OS Images for Server
images_OS = {
  "linux" = {
    "ubuntu" = "ubuntu-2204-lts"
    "ubuntu20" = "ubuntu-2004-lts"
    "debian" = "debian-12"
    "fedora" = "fedora-coreos-stable"
  }
}
```
![file-terraform.tfvars](docs/terraform/terraform3.png)


4. Terakhir, membuat file main.tf yang akan digunakan untuk membuat resource yang ingin dikelola pada infrastruktur.

```
# Create New VM Ubuntu
resource "google_compute_instance" "vm_instances_tabeldata" {
  for_each = var.vm_instances

  name = each.value.name
  machine_type = each.value.machine_type

  boot_disk {
    initialize_params {
      image = var.images_OS["linux"]["ubuntu20"]
    }
  }

  # Attach VPC and IP Static
  network_interface {
    network = google_compute_network.vpc_network_tabeldata.id
    subnetwork = google_compute_subnetwork.subet_network_tabeldata.id

    access_config {
      // Epheral public IP
      nat_ip = google_compute_address.ip_static_tabeldata[each.value.ip_static].address
    }
  }

  # Attach Firewall
  tags = each.value.tags

  # Metadata for SSH keys
  metadata = {
    ssh-keys = "crocox:${file("${path.module}/ssh_key.pub")}"
  }
}
```
![file-main.tf](docs/terraform/terraform4.png)




# Ansible



## Task 2 (Container)