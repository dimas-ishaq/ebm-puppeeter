---

##  Dokumentasi Instalasi Earnbitmoon Puppeeter

### 1. Install Termux

Unduh dan instal Termux melalui F-Droid atau situs resmi Termux.

> "You know lah"
---
### 2. Install Debian Menggunakan Proot-Distro

    pkg install proot-distro
    proot-distro install debian

Masuk ke lingkungan Debian:

    proot-distro login debian
---

###  3. Update dan Upgrade Sistem

    apt update && apt upgrade -y

---

###  4. Unduh Chromium ARM64

    wget http://ftp.cn.debian.org/debian/pool/main/c/chromium/chromium_135.0.7049.95-1_arm64.deb
---

### 5. Instal Chromium

Gunakan dpkg untuk instalasi:

    dpkg -i chromium_135.0.7049.95-1_arm64.deb

Jika muncul error karena dependensi, langsung perbaiki dan lanjutkan instalasi otomatis dengan:

    apt-get install -f


---

### 6. Cek Apakah Chromium Sudah Terinstal

Gunakan perintah which untuk memastikan chromium sudah terinstal:

    which chromium

Jika muncul output seperti /usr/bin/chromium, berarti Chromium berhasil terinstal.

### 7. Install Node.js

Untuk menginstal Node.js di dalam Debian (via Termux dan proot-distro), jalankan perintah berikut:

`apt install nodejs -y` 

Setelah itu, cek versi Node.js dan npm untuk memastikan instalasi berhasil:

    node -v
    npm -v

Jika output menampilkan versi dari Node.js dan npm, maka proses instalasi berhasil.

### 8. Cek dan Install Git

#### Cek apakah Git sudah terpasang:

Jalankan perintah berikut:

    git --version 

Jika muncul pesan seperti:

`bash: git: command not found` 

Berarti Git belum terinstal.

#### Install Git jika belum ada:

Pertama, update repositori:

    apt update

Kemudian install Git:

    apt install git -y

Setelah itu, cek ulang untuk memastikan Git sudah terinstal:

    git --version

Jika berhasil, akan muncul output seperti:

> git version 2.xx.x

---
### 10. Isi File `cookie.txt` dan `user-agent.txt`

Setelah clone repo dan masuk ke dalam folder `ebm-puppeeter`, kamu akan menemukan dua file berikut:

-   `cookie.txt`
    
-   `user-agent.txt`
    

Isi file tersebut dengan data yang sesuai:

#### ✏️ Edit `cookie.txt`:

    nano cookie.txt

Tempelkan isi cookie kamu (format string satu baris, bukan JSON), contohnya:

`sessionid=abc123; _ga=GA1.2.123456789.1234567890; other=value;` 

Tekan `CTRL+O`, lalu `Enter` untuk menyimpan. Tekan `CTRL+X` untuk keluar.

----------

#### ✏️ Edit `user-agent.txt`:

    nano user-agent.txt

Tempelkan User-Agent browser kamu, contohnya:

`Mozilla/5.0 (Linux; Android 11; SM-A107F) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.0.0 Mobile Safari/537.36` 

Simpan dan keluar seperti langkah sebelumnya.

### 11. Jalankan Bot dengan Node.js

Setelah `npm install` selesai dan file `cookie.txt` serta `user-agent.txt` sudah diisi, kamu bisa langsung menjalankan bot menggunakan perintah:

    node main.js


Dokumentasi ini disediakan untuk keperluan edukasi dan eksperimen pribadi.  

**Segala risiko penggunaan, pelanggaran kebijakan, atau kerugian akibat langkah-langkah dalam panduan ini sepenuhnya menjadi tanggung jawab pengguna.**  

Pastikan Anda memahami apa yang Anda lakukan dan tidak melanggar hukum atau ketentuan layanan pihak ketiga.
