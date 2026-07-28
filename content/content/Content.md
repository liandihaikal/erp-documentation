---
tags: [erp, modul, content]
---

# 🖥️ Content

⬅️ [[Home]]

## Ringkasan
Modul untuk mengelola konten yang ditampilkan ke publik/pelanggan, misalnya halaman website, kategori halaman, dan slide/banner promosi.

## Daftar Sub-Menu

| Sub-Menu | URL | Hak Akses | Fungsi |
|---|---|---|---|
| Page | `/admin/page` | `read-page` | Mengelola halaman konten (misal: halaman "Tentang Kami", promo) |
| Page Of Type | `/admin/page-of-type` | `read-page-type` | Mengelola kategori/tipe halaman |
| Slide | `/admin/slide` | `read-slide` | Mengelola slide/banner (misal untuk homepage) |

## Alur Penggunaan

### 1. Page Of Type (buat kategori dulu)
1. Buka **Content > Page Of Type**.
2. Tambah tipe halaman baru (misal: "Promo", "Artikel", "Info Perusahaan").
3. Simpan.

### 2. Page
1. Buka **Content > Page**.
2. Klik **Tambah Halaman**, pilih tipe halaman (dari Page Of Type), isi judul & isi konten.
3. Simpan/Publish.

### 3. Slide
1. Buka **Content > Slide**.
2. Upload gambar banner, atur urutan tampil dan link tujuan (jika slide bisa diklik).
3. Simpan.

## Keterkaitan dengan Modul Lain
Modul ini umumnya berdiri sendiri (untuk kebutuhan tampilan publik/website), tidak terhubung langsung ke alur transaksi seperti [[Sales|Penjualan]] atau [[Inventory|Inventaris]].
