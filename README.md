# Ambil-Lampiran-Gmail

Skrip Python otomatis untuk mengunduh lampiran dari akun Gmail berdasarkan kriteria pencarian, filter nama dokumen dan rentang tanggal yang spesifik.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

1.  **Python 3.x** terinstal di komputer.
2.  Akun Google/Gmail aktif.
3.  Akses internet untuk verifikasi API.

## Instalasi

1.  **Kloning atau Unduh** repository ini.
2.  Buka terminal/command prompt di folder project.
3.  Instal library Python yang dibutuhkan dengan perintah berikut:

```bash 
pip install google-api-python-client google-auth-httplib2 google-auth-oauthlib
```


## Konfigurasi Google Cloud Console
# Langkah 1: Buat Project & Aktifkan API
1. Buka Google Cloud Console.
2. Buat Project Baru.
3. Pergi ke APIs & Services > Library.
4. Cari "Gmail API", pilih hasilnya, lalu klik Enable.

# Langkah 2: OAuth Consent Screen
1. Pergi ke APIs & Services > OAuth consent screen.
2. Pilih External lalu klik Create.
3. Isi form yang wajib:
    - App Name: (Bebas, misal: Python Gmail Downloader)
    - User Support Email: Email Anda.
    - Developer Contact Email: Email Anda.
4. Klik Save and Continue (Lewati bagian "Scopes" jika ragu).
5. PENTING (Test Users):
    - Pada langkah Test Users, klik + ADD USERS.
    - Masukkan alamat email Gmail yang akan digunakan untuk proses masuk skrip ini.
    - Jika langkah ini dilewatkan, login akan gagal dengan error 403.

# Langkah 3: Unduh Credentials
- Pergi ke APIs & Services > Credentials.
- Klik + CREATE CREDENTIALS > OAuth client ID.
- Application type: Desktop app.
- Name: Desktop Client 1 (biarkan default).
- Klik Create.
- Unduh file JSON (klik ikon panah ke bawah).
- Ubah nama file tersebut menjadi credentials.json dan letakkan di folder yang sama dengan script python.

# Langkah 4: Konfigurasi
- Silakan konfigurasikan pengaturan di gmail.conf sesuai kebutuhan.
