---
tags: [erp, modul, approval]
---

# ✅ Permintaan Persetujuan (Approval Request)

⬅️ [[Home]]

## Ringkasan
Pusat notifikasi dan pemrosesan semua permintaan persetujuan (approval) yang butuh tindakan user — misalnya persetujuan Purchase Request, Purchase Order, cuti karyawan, atau dokumen lain yang alurnya diatur lewat **Workflow** (lihat [[Settings#Approval Workflow|Settings > Approval]]).

## Cara Mengakses
| Item | Keterangan |
|---|---|
| URL | `/admin/approval-request` |
| Hak Akses (permission) | `read-approval-request` |

## Alur Penggunaan
1. Buka menu **Permintaan Persetujuan** di sidebar.
2. Sistem menampilkan daftar dokumen yang menunggu persetujuan Anda (misal: Purchase Request dari divisi lain).
3. Klik salah satu item untuk melihat detail dokumen.
4. Pilih tindakan: **Setujui (Approve)** atau **Tolak (Reject)**, tambahkan catatan jika perlu.
5. Setelah disetujui, dokumen otomatis lanjut ke tahap berikutnya sesuai alur workflow (misal Purchase Request yang disetujui akan bisa dilanjutkan jadi [[Procurement#Purchase Order|Purchase Order]]).

⚠️ **Catatan:** Jenis dokumen apa saja yang masuk approval ditentukan oleh konfigurasi **Workflow** di menu [[Settings|Pengaturan]] > Approval. Jika suatu dokumen tidak butuh approval, prosesnya akan langsung lanjut tanpa masuk ke menu ini.

## Keterkaitan dengan Modul Lain
Modul ini menjadi "gerbang" bagi dokumen-dokumen dari modul [[Procurement|Pengadaan]], [[Sales|Penjualan]], [[HR]], dan lainnya yang butuh persetujuan berjenjang sebelum diproses lebih lanjut. 🔗
