# Project A: Web Portal Informasi & Manajemen Profil Akun In-Game

Web portal informasi interaktif berbasis Next.js yang terintegrasi dengan database PostgreSQL eksternal (host di Linux via jaringan Tailscale). Menyediakan portal konten informasi publik serta area personal pengguna untuk mengelola profil dan menautkan akun in-game mereka.

---

## Tech Stack

- **Framework:** Next.js 16 (App Router)
- **UI Library:** React 19 & React DOM 19
- **Bahasa:** TypeScript
- **Database:** PostgreSQL (Linux remote host via Tailscale)
- **ORM / Data Layer:** Prisma ORM
- **Runtime Lokal:** Node.js v26+, npm

---

## Ringkasan Fitur

- [ ] **Portal Informasi:** Halaman berita/artikel/panduan game dinamis dari database.
- [ ] **Autentikasi & Sesi:** Login akun, verifikasi kredensial, dan proteksi rute.
- [ ] **Profil Pengguna:** Halaman profil terintegrasi data database.
- [ ] **Manajemen Akun In-Game:** Penautan (*binding*), update, dan pemutusan akun in-game (IGN, UID, server/region).
- [ ] **UI Responsif:** Navbar dinamis (guest/auth), skeleton loading, dan error boundary.

---

## Menjalankan Proyek

### Prasyarat

1. Node.js `v20+` terpasang di mesin lokal.
2. Jaringan Tailscale aktif dan terhubung ke node Linux penyedia PostgreSQL.
3. File `.env.local` di root proyek dengan string koneksi database:
   ```env
   DATABASE_URL="postgresql://<USER>:<PASSWORD>@<IP_TAILSCALE_LINUX>:5432/<DB_NAME>?schema=public"
   ```

### Jalankan Dev Server

```bash
npm install
npm run dev
```

Buka [http://localhost:3000](http://localhost:3000) di browser.

---

## Log Pengembangan & Sesi

Seluruh catatan perkembangan teknis, serah-terima antar-sesi AI/developer, dan roadmap modular dicatat di direktori:

👉 **[Lihat Indeks Sesi Pengembangan (`sessions/README.md`)](sessions/README.md)**

