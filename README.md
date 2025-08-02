# CMS Monitoring Project (Firebase Version)

## Deskripsi
Project ini adalah aplikasi monitoring berbasis web yang menggunakan **Firebase Realtime Database** sebagai backend, dan HTML/JavaScript untuk frontend. Anda dapat menambah, mengedit, dan menghapus data project secara realtime tanpa PHP atau MySQL.

## Fitur
- Menampilkan daftar project secara realtime
- Tambah data project
- Edit data project
- Hapus data project
- Tersimpan langsung ke Firebase Realtime Database

## Teknologi yang Digunakan
- **Frontend:** HTML, CSS, JavaScript (Vanilla)
- **Database:** Firebase Realtime Database
- **Library Tambahan:** SweetAlert2 (untuk notifikasi)

## Cara Menjalankan

### 1. Clone Repository
```bash
git clone https://github.com/Rayhan-123-alt/CMSMonitoring.git
cd CMSMonitoring
2. Siapkan Firebase Project
Buat project di Firebase Console

Aktifkan Realtime Database → Mode "Test" (bebas baca/tulis sementara)

Salin konfigurasi dari halaman Project Settings → Tab General

js
Salin
Edit
// Contoh konfigurasi
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "your-app.firebaseapp.com",
  databaseURL: "https://your-app.firebaseio.com",
  projectId: "your-app",
  storageBucket: "your-app.appspot.com",
  messagingSenderId: "YOUR_SENDER_ID",
  appId: "YOUR_APP_ID"
};
3. Edit Kode
Buka index.html

Paste konfigurasi Firebase ke bagian <script> firebaseConfig

Sesuaikan jika perlu dengan struktur database (projects/)

4. Jalankan di Browser
Buka file index.html langsung di browser (double click atau via Live Server)

Struktur File
graphql
Salin
Edit
CMSMonitoring/
├── index.html         # Halaman utama (menampilkan data)
├── firebase.js        # Koneksi dan CRUD Firebase
├── style.css          # Tampilan UI
└── README.md          # Dokumentasi ini
Catatan
Tidak perlu XAMPP, PHP, atau MySQL.

Semua data tersimpan dan dikelola langsung melalui Firebase.

Untuk hosting, bisa pakai Firebase Hosting atau Netlify.

Lisensi
Open source, bebas dikembangkan.

yaml
Salin
Edit

---

Jika kamu ingin langsung saya buatkan file `README.md` di folder lokal atau ingin format markdown + copy-paste CLI siap pakai (misalnya buat deploy ke Firebase Hosting), tinggal bilang!