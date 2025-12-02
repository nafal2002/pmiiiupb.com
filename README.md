# Ringkasan Produk

**PMII UPB Official** adalah sistem informasi manajemen keanggotaan berbasis web untuk organisasi Pergerakan Mahasiswa Islam Indonesia (PMII) Komisariat Universitas Pelita Bangsa.

## Visi Produk

Menjadi platform digital terpadu yang memfasilitasi manajemen organisasi, kolaborasi antar kader, dan transparansi kegiatan PMII Komisariat UPB secara efisien dan modern.

## Tujuan Utama

1. **Digitalisasi Administrasi** - Mengelola data keanggotaan, kepengurusan, dan rayon secara terstruktur
2. **Transparansi Informasi** - Menyediakan akses informasi kegiatan, berita, dan dokumentasi organisasi
3. **Kolaborasi Kader** - Memfasilitasi komunikasi dan berbagi pengetahuan antar anggota
4. **Pelaporan & Analitik** - Menyajikan data statistik produktivitas rayon dan aktivitas kader

## Fitur Utama

### 🎯 Manajemen Keanggotaan
- Database kader lengkap dengan foto, biodata, dan riwayat kaderisasi
- Pengelompokan berdasarkan rayon, fakultas/prodi, dan tingkat kaderisasi
- Sistem role-based access control (Admin, Pengurus, Kader)
- Export data dan cetak Kartu Tanda Anggota (KTA) dengan QR Code

### 📰 Portal Berita & Informasi
- Sistem publikasi berita/artikel dengan kategori dan tag
- Fitur komentar untuk diskusi antar kader
- Editor rich-text untuk konten yang menarik
- Galeri foto dokumentasi kegiatan organisasi

### 📅 Manajemen Kegiatan
- Kalender agenda kegiatan rayon dan komisariat
- Tracking hari besar nasional dan keagamaan
- Notifikasi kegiatan mendatang

### 📚 Perpustakaan Digital
- Repository e-book, dokumen, dan materi kaderisasi
- Support format PDF, Word, Excel
- Sistem kategorisasi buku berdasarkan topik
- Akses mudah untuk semua anggota

### 👥 Profil & Networking
- Profil kader yang dapat dikustomisasi
- Informasi struktur kepengurusan
- Directory kontak anggota berdasarkan rayon
- Quotes inspiratif dari tokoh dan kader

### 📊 Dashboard & Analitik
- Statistik keanggotaan real-time
- Grafik produktivitas per rayon
- Laporan aktivitas dan partisipasi kader
- Visualisasi data yang interaktif

### 💬 Komunikasi & Aspirasi
- Form kontak untuk aspirasi dan masukan
- Sistem notifikasi email
- Integrasi dengan media sosial

## Hierarki Pengguna

### 1. Super Admin (role_id: 1)
- Akses penuh ke seluruh sistem
- Manajemen user dan role
- Konfigurasi sistem

### 2. Admin/Pengurus (role_id: 2)
- Manajemen konten (berita, galeri, perpustakaan)
- Manajemen data kader dan rayon
- Moderasi komentar dan konten

### 3. Pengurus Rayon (role_id: 3)
- Upload konten untuk rayon
- Manajemen anggota rayon
- Akses dashboard rayon

### 4. Kader/Anggota (role_id: 4+)
- Akses baca konten
- Manajemen profil pribadi
- Komentar dan interaksi
- Akses perpustakaan

## Konteks Domain

### Entitas Utama
- **Users** - Akun pengguna dengan autentikasi
- **Kader** - Data lengkap anggota PMII UPB
- **Rayon** - Cabang organisasi di tingkat fakultas/prodi
- **Posts** - Artikel, berita, dan konten blog
- **Categories** - Kategori konten (Berita, Opini, Kegiatan, dll)
- **Tags** - Label untuk konten (kaderisasi, sosial, akademik, dll)
- **Agenda** - Jadwal kegiatan dan event
- **Galeri** - Dokumentasi foto kegiatan
- **Perpus** - Repository e-book dan dokumen
- **Pengurus** - Struktur kepengurusan komisariat
- **Quotes** - Kutipan inspiratif
- **Profile** - Informasi organisasi
- **Comments** - Komentar pada artikel
- **Contacts** - Pesan aspirasi dari pengunjung

### Relasi Penting
- User → Kader (one-to-one)
- User → Rayon (many-to-one)
- User → Posts (one-to-many)
- Post → Category (many-to-one)
- Post → Tags (many-to-many)
- Post → Comments (one-to-many)

## Teknologi Inti

- **Backend**: Laravel 10 + PHP 8.1
- **Frontend**: React 18 + TypeScript + Inertia.js
- **Styling**: Tailwind CSS + Bootstrap Icons
- **Database**: MySQL
- **Build**: Vite (dengan SSR support)

## Target Pengguna

1. **Pengurus Komisariat** - Untuk administrasi dan manajemen organisasi
2. **Kader PMII UPB** - Untuk akses informasi dan networking
3. **Calon Anggota** - Untuk mengenal organisasi
4. **Alumni** - Untuk tetap terhubung dengan organisasi

## Catatan Migrasi

⚠️ Aplikasi ini dikembangkan untuk PMII Komisariat UPB (Universitas Pelita Bangsa). 

Referensi legacy yang mungkin masih ditemukan:
- Domain : `pmiiiupb.com`
- Email admin: `admin@pmiiiupb.com`

Lihat `migration-upb.md` untuk detail lengkap proses migrasi.
