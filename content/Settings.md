---
tags: [erp, modul, settings]
---

# ⚙️ Pengaturan (Settings)

⬅️ [[Home]]

## Ringkasan
Modul administrasi sistem — mengatur data referensi umum, alur approval (workflow), hak akses user & role, serta pengaturan umum aplikasi. Modul ini biasanya hanya diakses oleh Admin/IT.

## Daftar Sub-Menu

| Sub-Menu | URL | Hak Akses | Fungsi |
|---|---|---|---|
| Reference | `/admin/lookup` | `read-lookup` | Data referensi/lookup umum sistem |
| **Approval** > Workflow | `/admin/workflow` | `read-workflow` | Mengatur alur persetujuan berjenjang tiap jenis dokumen |
| **Authorization** > Action | `/admin/action` | `read-action` | Daftar aksi/permission yang tersedia di sistem |
| **Authorization** > Role | `/admin/role` | `read-role` | Mengatur peran/jabatan dan permission yang dimiliki |
| **Authorization** > Module | `/admin/module` | `read-module` | Mengatur modul yang tersedia di sistem |
| **Authorization** > User | `/admin/user` | `read-user` | Mengatur akun pengguna sistem |
| General Settings | `/admin/setting` | `update-setting` | Pengaturan umum aplikasi (nama perusahaan, logo, dll) |

---

## 1. Reference (Lookup)
**Fungsi:** Mengelola data referensi kecil yang dipakai di berbagai form sistem (misal: satuan unit, status, dll — tergantung implementasi).

## 2. Approval > Workflow ⭐ (Penting)
**Fungsi:** Menentukan dokumen apa saja yang butuh persetujuan berjenjang, dan siapa yang berhak menyetujui di tiap tahap.

**Langkah Umum:**
1. Buka **Pengaturan > Approval > Workflow**.
2. Pilih jenis dokumen (misal: Purchase Request, Cash Disbursement).
3. Atur urutan approval (misal: Supervisor → Manager → Direktur) dan syarat tiap tahap (misal berdasarkan nominal).
4. Simpan.

🔗 Alur yang diatur di sini akan muncul otomatis di [[Approval-Request|Permintaan Persetujuan]].

## 3. Authorization (Hak Akses) ⭐ (Penting)

### Action
Daftar seluruh permission/aksi yang tersedia di sistem (misal `read-payroll`, `update-setting`) — biasanya sudah didefinisikan sistem, jarang diubah manual.

### Role
Mengelompokkan sekumpulan **Action/permission** menjadi satu peran (misal: role "HRD" diberi akses `read-attendance`, `read-payroll`, dst).

**Langkah Umum:**
1. Buka **Pengaturan > Authorization > Role**.
2. Buat role baru atau edit role yang ada.
3. Centang permission yang boleh diakses role tersebut.
4. Simpan.

### Module
Mengatur modul apa saja yang aktif/tersedia untuk ditampilkan di sistem.

### User
Mengelola akun pengguna dan menetapkan role ke masing-masing user.

**Langkah Umum:**
1. Buka **Pengaturan > Authorization > User**.
2. Tambah user baru, isi data & assign role yang sesuai (misal: role "HRD", "Kasir", "Sales").
3. Simpan — user langsung mendapat akses sesuai permission dari role-nya.

⚠️ **Alur pengaturan hak akses yang benar:** buat **Role** dulu (dengan permission-nya) → baru assign role tersebut ke **User**.

## 4. General Settings
**Fungsi:** Pengaturan umum aplikasi seperti identitas perusahaan, logo, format tanggal/mata uang, dll.

## Keterkaitan dengan Modul Lain
Modul ini mengontrol **siapa boleh mengakses apa** di seluruh modul lain, dan mengatur **alur approval** yang dipakai [[Approval-Request|Permintaan Persetujuan]] di semua modul transaksi.
