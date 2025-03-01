# Pembuat Folder Massal

[![Bahasa Indonesia](https://img.shields.io/badge/lang-Indonesia-red)](README.id.md)  
[![English](https://img.shields.io/badge/lang-English-blue)](README.md)

**Pembuat Folder Massal** adalah proyek yang berisi skrip Python untuk secara otomatis membuat banyak subfolder dalam folder utama yang ditentukan. Ini berguna untuk dengan cepat membuat banyak folder guna mengorganisir file atau untuk keperluan pengujian.

## Fitur

- Membuat sejumlah subfolder dengan nama yang dapat disesuaikan.
- Memungkinkan penyesuaian jalur folder utama.
- Mendukung penambahan awalan (prefix) pada nama folder untuk organisasi yang lebih baik.
- Memberikan umpan balik yang jelas di terminal menggunakan tag status:
  - `[Info]` untuk informasi umum.
  - `[Success]` untuk folder yang berhasil dibuat.
  - `[Skip]` untuk folder yang sudah ada.
  - `[Error]` untuk input tidak valid atau masalah lainnya.
- Mencegah terminal tertutup secara otomatis setelah eksekusi, sehingga pengguna dapat meninjau hasilnya.

## Persyaratan

- Python 3.x harus terinstal di sistem Anda.

## Cara Penggunaan

### Langkah 1: Kloning Repository

Untuk memulai, kloning repository ini ke komputer Anda menggunakan metode sparse checkout agar hanya mendapatkan file proyek yang diperlukan.

```bash
git clone --no-checkout https://github.com/bektidk/ffos.git
cd ffos
git sparse-checkout init --cone
git checkout main
git sparse-checkout set mass-folder-builder
cd mass-folder-builder
```

### Langkah 2: Jalankan Skrip

Buka terminal atau command prompt, navigasikan ke direktori proyek, lalu jalankan skrip berikut:

```bash
python create_folders.py
```

### Langkah 3: Masukkan Detail

Skrip akan meminta beberapa input berikut:

- Jalur Folder Utama: Tentukan direktori tempat subfolder akan dibuat.
- Awalan Folder: Secara opsional, tambahkan awalan pada nama folder (misalnya, "Folder "). Biarkan kosong jika tidak ingin menambahkan awalan.
- Jumlah Folder: Masukkan jumlah folder yang akan dibuat.

### Langkah 4: Periksa Hasilnya

Setelah skrip selesai dijalankan, Anda akan menemukan subfolder yang telah dibuat dalam folder utama yang ditentukan. Nama folder akan berurutan dan diawali dengan awalan jika sudah ditentukan. Terminal akan tetap terbuka, memungkinkan Anda untuk meninjau hasilnya.

## Contoh

Berikut adalah contoh sesi penggunaan:

```bash
----------------------------------------
Selamat datang di Mass Folder Builder!
----------------------------------------
Masukkan jalur folder utama: G:/Proyek Saya
Masukkan awalan untuk folder (kosongkan jika tidak ada): Folder
Masukkan jumlah folder yang akan dibuat: 5
----------------------------------------
Membuat 5 folder di: G:/Proyek Saya
----------------------------------------

[Info] Folder utama sudah ada di: G:/Proyek Saya
[Success] Folder 'Folder 1' berhasil dibuat.
[Success] Folder 'Folder 2' berhasil dibuat.
[Success] Folder 'Folder 3' berhasil dibuat.
[Success] Folder 'Folder 4' berhasil dibuat.
[Success] Folder 'Folder 5' berhasil dibuat.

----------------------------------------
Proses selesai! Periksa folder Anda.
----------------------------------------

Tekan Enter untuk keluar...
```

## Catatan

- Pastikan direktori yang ditentukan sudah ada sebelum menjalankan skrip, karena skrip tidak akan membuat folder utama jika belum ada.
- Jika sebuah folder sudah ada, skrip akan memberi tahu Anda dan melewati pembuatan folder tersebut.
- Gunakan awalan yang bermakna untuk mengorganisir folder dengan lebih baik.
- Skrip akan menunggu Anda menekan Enter sebelum menutup terminal.
