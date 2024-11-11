# Pre-Test Bootcamp DevOps

## knowledge base

1. Apa yang anda ketahui tentang DevOps?
2. Apa yang anda ketahui tentang Infrastructure?
3. Apa yang anda ketahui tentang server, sebutkan implementasi berserta contohnya?
4. Mengapa server dibutuhkan dalam pengembangan/development suatu software?
5. Apa yang anda ketahui mengenai Virtualisasi dan Container?
6. Mengapa teknology container saat ini sangat populer?
7. Apa yang anda ketahui tentang Orchestration Container System?

Cara pengerjaan, silahkan update file ini tulis jawabanya di bawah ini

### Jawaban

1. DevOps merupakan sebuah prinsip developer yang menjadi penghubung antara tim development (programmer) dan operations (infrastruktur) yang bertugas untuk mempercepat proses pengembangan, pengujian, hingga rilis suatu produk (aplikasi/sistem) kepada publik. Metode ini menggunakan konsep "CI/CD (Continuous Integration dan Continuous Deployment)" yang memungkinkan pembaharuan terhadap produk secara terus-menerus tanpa adanya gangguan sistem.

    Berikut adalah Proses pengembangan siklus hidup DevOps:

    ```
    a. Plan: Proses perencanaan untuk membuat flow atau alur kerja sebelum tim developer menulis suatu kode (Test Case).
    b. Code: Proses atau tahap dari tim developer dalam membuat sebuah kode untuk suatu produk yang akan dibuat dan dikembangkan.
    c. Build: Proses yang dilakukan untuk mengonversi kode menjadi aplikasi yang nantinya dapat dieksekusi pada tahap pengujian.
    d. Test: Proses pengujian untuk mendeteksi adanya bug atau tidak dan memastikan bahwa kode yang dihasilkan memenuhi persyaratan.
    e. Release: Proses persiapan kode yang sudah lolos pengujian menuju tahap produksi.
    f. Deploy: Proses deployment untuk produk yang akan dijalankan pada server secara otomatis maupun manual.
    g. Operate: Proses untuk memastikan apakah layanan produk berjalan dengan lancar atau tidak.
    h. Monitor: Proses pemantauan berkelanjutan terhadap aplikasi dan infrastruktur produk.
    ```

2. Infrastruktur merupakan suatu sistem, perangkat, dan layanan yang diperlukan untuk menjalankan dan mengelola sebuah perusahaan di lingkungan teknologi, mencakup komponen fisik seperti perangkat keras (hardware), perangkat lunak (software), jaringan, penyimpanan, dan layanan cloud.

    Berikut Jenis-jenis dari Infrastruktur:

    ```
    a. Infrastruktur Lokal (On-Premises): Model infrastruktur dimana seluruh perangkat keras dan lunak secara fisik berada pada perusahaan dan dikelola oleh staff yang bertugas.
    b. Infrastruktur Cloud: Model infrastruktur yang disediakan oleh penyedia cloud computing dan tidak perlu dikelola secara fisik.
    c. Infrastruktur Hybrid: Model infrastruktur yang menggabungkan infrastruktur lokal dan cloud sehingga memungkinkan perusahaan untuk mengontrol secara fleksibel.
    ```

  Infrastuktur dalam Devops biasanya disebut dengan IaC (Infrastructure as a Code) yang digunakan untuk mengelola dan menyediakan infrastruktur menggunakan kode dan alat otomatisasi (Terraform, Ansible). Dengan menggunakan IaC, maka infrastruktur perusahaan dapat dikelola menjadi lebih efisien dan minim dari kesalahan.

3. Server merupakan sistem yang menyediakan layanan atau sumber daya ke komputer lain di dalam jaringan. Server juga umumnya lebih baik dibandingkan dengan komputer biasa, yang memiliki kemampuan pemrosesan, penyimpanan, dan jaringan yang lebih baik.

    Berikut implementasi server beserta contohnya:

    ```
    a. Web Server: Sebuah software yang memberikan layanan berupa data dan berfungsi untuk menerima permintaan HTTP atau HTTPS dari client (web browser). Contohnya adalah Nginx dan Apache
    b. DNS Server: Sebuah sistem yang berfungsi untuk menerjemahkan nama domain (www.domain.com) yang mudah diingat menjadi alamat IP sehingga dapat diakses oleh client. Contohnya BIND (Berkeley Internet Name Domain)
    c. Database Server: Sebuah program komputer yang memberikan layanan untuk mengelola dan menyediakan akses ke basis data untuk aplikasi dalam suatu jaringan. Contohnya MySQL, PostgreSQL, dsb
    ```

4. Server sangatlah dibutuhkan dan penting dalam pengembangan perangkat lunak (software) karena berfungsi untuk menyimpan dan mengakses file yang dibutuhkan oleh pengguna dan juga menyediakan lingkungan yang stabil dalam melakukan tahapan pengembangan. Disini server mendukung banyak aspek penting dalam pengembangan perangkat lunak dari kolaborasi, pengujian, keamanan, sampai dengan memastikan apakah proses pengembangan berjalan dengan efisien dan sesuai standar yang diharapkan atau tidak.

5. Virtualisasi merupakan teknologi yang dapat membagi resource besar menjadi lebih kecil. Secara sederhana kita dapat menjalankan beberapa sistem operasi secara bersamaan menggunakan hypervisor. Hypervisor dalam virtualisasi adalah program untuk membuat dan menjalankan mesin virtual (VM) seperti VMware, dsb.

Containerisasi merupakan sebuah metode atau teknik yang memungkinkan aplikasi dapat berjalan dalam lingkungan terisolasi tanpa harus menjalankan sistem operasi di setiap server yang terhubung. Containerisasi dijalankan menggunakan engine seperti docker ataupun kubernetes yang memungkinkan aplikasi dapat berjalan pada sistem operasi yang sama.

  Berikut perbandingan utama antara virtualisasi dan containerisasi:

  ```
  a. Pengelolaan: Kontainer lebih cepat dikelola dan diterapkan daripada virtual machine.
  b. Keamanan: Virtual Machine memiliki keamanan yang lebih tinggi, sedangkan kontainer berisiko jika ada kerentanan di kernel.
  c. Penggunaan: Virtual Machine cocok digunakan untuk aplikasi yang memerlukan sistem operasi berbeda, sedangkan kontainer cocok untuk aplikasi mikro-service.
  d. Ukuran: Kontainer memiliki ukuran yang lebih kecil, sedangkan virtual machine memiliki ukuran yang lebih besar.
  ```

6. Teknologi kontainer (docker & kubernetes) saat ini sangatlah populer dikarenakan beberapa alasan utama yang membuatnya ideal untuk melakukan pengembangan, distribusi, dan manajemen aplikasi.

    Berikut alasan mengapa teknologi kontainer sangat populer:

    ```
    a. Efisiensi Sumber Daya yang Tinggi
      Kontainer sangat efisien dalam penggunaan sumber daya, dapat memulai dengan cepat, dan memiliki ukuran yang lebih kecil dibandingkan dengan mesin virtual. Sehingga penggunaan CPU, Memori, dan penyimpanan yang dihasilkan lebih efisien

    b. Skalabilitas dan Fleksibilitas
      Kontainer memungkinkan kita dengan mudah untuk melakukan skalabilitas aplikasi sesuai dengan kebutuhan. Kita dapat menambah dan mengurasi jumlah instance kontainer secara dinamis yang memberikan fleksibiltas tinggi untuk dapat mengelola aplikasi yang memiliki fluktuasi (ketidaktepatan) dalam penggunaan sumber daya.
    
    c. Penghematan Biaya
      Dikarenakan kontainer memiliki ukuran yang kecil dan ringan, perusahaan dapat menghemat biaya pada infrastruktur komputasi cloud. Kontainer memungkinkan perusahaan untuk menggunakan lebih sedikit instance cloud, yang berujung pada penghematan biaya yang signifikan.
    ```

  Teknologi kontainer pada saat ini sangatlah membantu perusahaan/organisasi dalam mengembangkan, menguji, dan mengelola suatu aplikasi/sistem dengan lebih cepat, aman, efisien, dan sebagainya yang menjadikannya salah satu teknologi terbaik dalam era digital saat ini.

7. Orchestration Container System merupakan sebuah proses untuk mengotomatiskan jaringan dan pengelolaan kontainer sehingga kita dapat menerapkan aplikasi dalam skala besar. Orchestration Container bertujuan untuk menyederhanakan manajemen infrastruktur kontainer dengan mengotomatiskan siklus hidup, mulai dari penyediaan, penjadwalan sampai deployment dan penghapusan.

    Berikut beberapa manfaat dari Orchestration Container System:

    ```
    a. Menyeimbangkan beban aplikasi dan manajemen lalu lintas pada server.
    b. Kemanan yang baik di seluruh kontainerisasi.
    c. Pemantauan ataupun monitoring terhadap status kontainer yang ada.
    ```


## Task 1 (Virtualization)

- Buatlah sebuah VM dengan kententuan
  - username: `<github_user>` contoh `dimasm93`
  - hostname: `<email_without_at>` contoh `dimas.tabeldata.com`
  - OS: `ubuntu-20.04` atau `centos-7`
- Install webserver `nginx`
- Buatlah web profile temen-temen kemudian deploy ke webserver nginx tersebut yang telah di deploy
  
(kirimkan hasil screenshotnya simpan dalam folder `screenshot` dengan nama `task1.png`)

## Task 2 (Container)

Jika saya memiliki architecture seperti berikut:

![container-apps](docs/images/01-container.png)

Dimana berikut adalah configurasi docker image:

1. Backend container
  - image: `dimmaryanto93/udemy-springboot-app:latest`
  - port: `8080`
  - env: 
    - `DATABASE_HOST`: `<ip-domain-db>`
    - `DATABASE_PORT`: `5432` 
    - `DATABASE_NAME`: `<db-name>`
    - `DATABASE_PASSWORD`: `<db-password>`
    - `APPLICATION_PORT`: `8080`
  need:
    - Database PostgreSQL v14.2
2. Frontend container
  - image: `dimmaryanto93/udemy-angular-app:latest`
  - port: `80`
  - env:
    - `APPLICATION_PORT`: `80`
    - `NGINX_ROOT_DOCUMENT`: `/var/www/html`
    - `BACKEND_HOST`: `<ip-backend-apps>`
    - `BACKEND_PORT`: `<port-backend-apps>`
    - `BACKEND_CONTEXT_PATH`: `/`
  - need:
    - Backend container

Silahkan buat docker-compose filenya, kemudian simpan dalam folder `tasks` dengan nama `docker-compose.yaml`

