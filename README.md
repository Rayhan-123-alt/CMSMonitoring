# CMS Monitoring Project

## Deskripsi
Project ini adalah aplikasi monitoring project berbasis web menggunakan PHP dan MySQL. Anda dapat menambah, mengedit, dan menghapus data project melalui antarmuka web.

## Fitur
- Tambah project
- Edit project
- Hapus project
- List project

## Cara Menjalankan Tanpa XAMPP

### 1. Persyaratan
- PHP (disarankan versi 7.4 atau lebih baru)
- MySQL/MariaDB
- Web browser

### 2. Instalasi di Mac/Linux

#### a. Install PHP dan MySQL
**Mac (menggunakan Homebrew):**
```bash
brew install php
brew install mysql
brew services start mysql
```

**Linux (Debian/Ubuntu/Armbian):**
```bash
sudo apt update
sudo apt install apache2 php libapache2-mod-php php-mysql mariadb-server
sudo systemctl start apache2
sudo systemctl start mariadb
```

#### b. Setup Database
1. Login ke MySQL:
   ```bash
   mysql -u root -p
   ```
2. Buat database dan import file `database_setup.sql`:
   ```sql
   CREATE DATABASE nama_database;
   USE nama_database;
   SOURCE /path/ke/database_setup.sql;
   ```
3. Edit file `db.php` dan sesuaikan nama database, username, dan password.

#### c. Jalankan Web Server
**Opsi 1: PHP Built-in (untuk development)**
```bash
cd /path/ke/CMSMonitoringProject
php -S localhost:8000
```
Akses di browser: [http://localhost:8000](http://localhost:8000)

**Opsi 2: Apache/Nginx**
- Copy semua file ke folder web server, misal `/var/www/html/`
- Akses via browser sesuai alamat server

## Catatan
- Tidak perlu XAMPP, cukup PHP dan MySQL/MariaDB.
- Untuk production, disarankan menggunakan Apache/Nginx.
- Jika ada error koneksi database, cek konfigurasi di `db.php`.

## Struktur File
- `index.php` : Halaman utama
- `add_project.php` : Tambah project
- `edit_project.php` : Edit project
- `delete_project.php` : Hapus project
- `db.php` : Koneksi database
- `database_setup.sql` : Struktur database
- `style.css` : Style tampilan
- `user.php` : (opsional, jika ada fitur user)