# Sesi 01: Koneksi PostgreSQL & Introspeksi Skema

## Ringkasan Tugas
Menghubungkan aplikasi Next.js di Windows ke instance PostgreSQL yang berjalan di mesin Linux melalui koneksi jaringan Tailscale, lalu melakukan introspeksi skema database eksisting menggunakan Prisma ORM.

## Lingkup Pekerjaan
1. Memverifikasi koneksi port PostgreSQL (default: `5432`) dari Windows ke Linux via IP Tailscale.
2. Mengonfigurasi `DATABASE_URL` di `D:\Code\Project\project_a\.env.local`.
3. Memasang dependensi Prisma (`prisma`, `@prisma/client`).
4. Menjalankan `npx prisma db pull` untuk menyalin struktur tabel eksisting ke `prisma/schema.prisma`.
5. Menjalankan `npx prisma generate` untuk men-generate TypeScript client.
6. Membuat file singleton Prisma client di `src/lib/prisma.ts`.
7. Menguji query data awal untuk membuktikan koneksi berhasil dan membaca struktur tabel user/akun game.

## Kriteria Selesai (Definition of Done)
- [ ] Koneksi port 5432 terkonfirmasi sukses via Tailscale.
- [ ] File `prisma/schema.prisma` terisi model tabel hasil introspeksi nyata dari DB Linux.
- [ ] Modul `src/lib/prisma.ts` siap dipakai oleh Server Components dan Server Actions.
