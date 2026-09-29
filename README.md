# Giveaway Checker

Validasi otomatis pemenang giveaway Instagram dari ribuan komentar — keyword, hashtag, jumlah tag, dan anti-duplikasi, tanpa perlu cek satu-satu.

**100% berjalan di browser (client-side).** Tidak ada data yang dikirim ke server mana pun — semua pemrosesan terjadi langsung di perangkat pengguna.

## Fitur

- **Upload file komentar** — baca langsung dari file hasil "Save As → Webpage, Complete" pada halaman postingan Instagram, atau tempel manual (format `username | komentar`). Mendukung `.html`, `.txt`, dan `.csv`.
- **Merge otomatis** — komentar ganda dari akun yang sama digabung jadi satu entri, supaya satu akun tidak mendapat peluang undian berkali-kali.
- **Kriteria fleksibel**:
  - Keyword wajib (cocok longgar atau persis)
  - Jumlah tag minimal
  - Hashtag wajib
  - Minimal panjang komentar
  - Blacklist akun
  - Filter kata terlarang/spam
  - Satu akun = satu entri (bisa dimatikan)
  - Abaikan tag ke diri sendiri
- **Hasil interaktif** — filter cepat "Tampilkan yang Lolos" / "Tampilkan Semua", plus rincian alasan gugur per kriteria.
- **Tautan langsung ke profil** — username dan akun yang di-tag jadi link yang bisa langsung diklik untuk verifikasi manual.
- **Undi pemenang & ekspor CSV** — acak pemenang dari daftar yang sudah tervalidasi, atau unduh hasilnya untuk diproses lebih lanjut.

## Cara Pakai

Lihat [`cara_pakai.txt`](./cara_pakai.txt), atau klik tombol **"Baca cara pakai"** di dalam aplikasi.

## Menjalankan

Tool ini adalah file statis — tidak butuh build step atau backend.

**Opsi 1 — GitHub Pages**
1. Fork/clone repo ini
2. Aktifkan GitHub Pages dari branch utama
3. Buka URL GitHub Pages yang dihasilkan

**Opsi 2 — Lokal**
```
git clone <repo-ini>
cd <folder-repo>
# buka index.html langsung, atau jalankan local server (disarankan agar fitur "Baca cara pakai" berfungsi):
python3 -m http.server 8000
```

> Catatan: fitur "Baca cara pakai" memuat `cara_pakai.txt` lewat `fetch()`, yang diblokir browser saat file dibuka langsung (`file://`). Gunakan GitHub Pages atau local server untuk fitur ini berjalan penuh.

## Keterbatasan yang Perlu Diketahui

- **Bukan alat resmi Instagram/Meta.** Tool ini hanya membaca file yang sudah kamu simpan sendiri di komputer — tidak melakukan scraping otomatis ke Instagram.
- Follow, share, dan status akun publik/private **tidak bisa** diverifikasi otomatis — tetap perlu dicek manual untuk daftar akhir yang lolos.
- Akurasi ekstraksi dari file HTML bergantung pada struktur halaman Instagram saat file disimpan; jika Instagram mengubah struktur halamannya, parser mungkin perlu disesuaikan.

## Disclaimer

Tool ini **tidak terafiliasi resmi dengan Instagram atau Meta Platforms, Inc.** Segala bentuk pengambilan data dari Instagram — termasuk cara pengguna memperoleh file yang diunggah ke tool ini — sepenuhnya menjadi tanggung jawab pengguna, dan wajib mengikuti Ketentuan Layanan resmi dari Meta.

## Lisensi

MIT License — lihat [`LICENSE`](./LICENSE).

## Kredit

Made by [apink.web.id](https://apink.web.id) with Claude · © 2026 · versi 1.2
