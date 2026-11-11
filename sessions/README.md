# Indeks Sesi Pengembangan Proyek

Dokumen ini melacak seluruh progres kerja modular per sesi. Setiap sesi memiliki fokus isolasi sendiri agar konteks tetap terjaga saat berganti sesi chat atau berganti pengembang.

---

## Tabel Roadmap & Status Sesi

| No | Folder Sesi | Topik / Fitur | Status | Target Utama |
| :---: | :--- | :--- | :---: | :--- |
| **01** | [`01-koneksi-db`](01-koneksi-db/) | Koneksi PostgreSQL & Introspeksi Skema | **IN PROGRESS** | Koneksi Tailscale, `.env.local`, `prisma db pull` |
| **02** | [`02-auth`](02-auth/) | Autentikasi Pengguna & Proteksi Rute | NOT STARTED | Login, hash verify, cookie session, middleware |
| **03** | [`03-profile-ingame`](03-profile-ingame/) | Modul Profil & Penautan Akun In-Game | NOT STARTED | Tampilan profil, relasi user-game, form binding |
| **04** | [`04-content-portal`](04-content-portal/) | Portal Informasi Publik | NOT STARTED | Feed artikel, detail info, dynamic SEO |
| **05** | [`05-ui-layout`](05-ui-layout/) | Navigasi, Desain Sistem & Error State | NOT STARTED | Navbar auth-aware, skeleton, fallback UI |
| **06** | [`06-build-audit`](06-build-audit/) | Validasi Skema, Testing & Build Audit | NOT STARTED | Zod validation, `npm run build`, final checklist |

---

## Panduan Melanjutkan Kerja di Sesi Baru

Bila membuka sesi baru, cukup rujuk folder sesi yang sedang aktif:

> *"Lanjutkan kerja pada folder `sessions/01-koneksi-db/`"*

AI/rekan pengembang akan membaca:
1. `BRIEF.md`: Memahami lingkup tugas sesi tersebut.
2. `PROGRESS.md`: Mengetahui apa yang sudah selesai dan **langkah konkret berikutnya**.

---

## Konvensi Kerja Tiap Sesi

1. **Pembuatan Folder Bertahap:** Folder sesi berikutnya (02, 03, dst.) dibuat saat sesi aktif selesai. Spesifikasi sesi baru disusun berdasarkan temuan riil (misal skema tabel atau library yang terpilih).
2. **Kedaulatan File & Eksekusi:** Selalu ajukan rencana/draft sebelum menulis atau mengubah file aplikasi. Eksekusi perubahan dilakukan setelah konfirmasi user.
3. **Kedaulatan Git:** Perintah Git dijalankan mandiri oleh user; jangan mengeksekusi operasi git secara otomatis.
4. **Handoff Wajib:** Setiap kali pekerjaan dijeda atau selesai, agen/developer wajib memperbarui file `PROGRESS.md` di folder sesi aktif dan memperbarui tabel status di atas.
