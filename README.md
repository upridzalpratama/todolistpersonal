# Questline

To-do & goals gamified — satu file `index.html`, tanpa server, tanpa build, data di `localStorage` (key `questline.v1`).

**Pakai:** buka `index.html` di browser (boleh via `file://`) atau host statis (mis. GitHub Pages).

## Fitur
- Hierarki Epic tahunan → Quest bulanan → Task harian, progress roll-up otomatis
- XP & level (`XP = 10 × D × (1 + min(0.05·streak, 0.5))`, level n butuh `50n(n−1)` XP), streak + Streak Freeze, coin & Reward Shop
- Boss Battle bulanan, 7 badge, task berulang, review bulanan & rekap tahunan, heatmap 365 hari
- Export/import JSON (validasi skema + snapshot `questline.v1.backup`), arsip tahun lama, deteksi kuota penuh
- Tema gelap/terang, responsif (bottom nav di mobile), keyboard: `N` task baru, `/` cari, `1–3` pindah tab

## Keputusan di luar PRD
- Coin: ±1 coin per 10 XP.
- Anti-akal-akalan: task dengan judul + tanggal sama hanya memberi XP sekali (hapus-buat-ulang tidak menambah XP); bonus Quest/Boss butuh minimal 3 task; Epic tuntas butuh minimal 3 Quest tuntas.
- Streak putus tepat tengah malam (waktu lokal).
