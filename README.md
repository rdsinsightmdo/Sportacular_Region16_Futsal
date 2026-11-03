# Klasemen Turnamen Futsal BRI Region 16 Manado

| File | Untuk siapa | Fungsi |
|---|---|---|
| `index.html` | User / penonton | Hanya lihat. Membaca `data.json` dan memperbarui tampilan sendiri tiap 30 detik. |
| `admin.html` | Panitia | Isi nama tim dan skor, lalu klik **Publikasikan** untuk menyimpan ke `data.json` di repo ini. |
| `data.json` | — | Data klasemen. Diubah otomatis dari halaman admin. |

## Pemasangan (sekali saja)

1. Buat repo baru di GitHub (misal `futsal-bri`), upload ketiga file ini.
2. Buka **Settings → Pages**, pilih *Deploy from a branch*, branch `main`, folder `/ (root)`, lalu Save.
   Setelah sekitar 1 menit, situs aktif di `https://<username>.github.io/futsal-bri/`.
3. Buat token: **Settings akun → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**.
   - Repository access: *Only select repositories* → pilih repo ini saja.
   - Permissions → Repository permissions → **Contents: Read and write**.
   - Salin tokennya (diawali `github_pat_`).
4. Buka `https://<username>.github.io/futsal-bri/admin.html`, buka panel **Publikasi ke GitHub**, isi username, nama repo, dan token. Pengaturan ini hanya tersimpan di browser perangkat admin.

## Pemakaian

- Bagikan ke user: `https://<username>.github.io/futsal-bri/` (halaman `index.html`).
- Admin mengisi skor di `admin.html`, lalu klik **Publikasikan sekarang**, atau centang **Publikasi otomatis**.
- Perubahan terlihat di halaman user sekitar 1 menit kemudian (waktu proses GitHub Pages).
- Pindah perangkat admin: isi pengaturan yang sama, lalu klik **Ambil data dari GitHub**.

## Catatan keamanan

- `admin.html` bisa saja dibuka orang lain jika tahu alamatnya, tetapi tanpa token mereka **tidak bisa** mempublikasikan apa pun.
- Jangan pernah menulis token di dalam file atau membagikannya. Jika token bocor, hapus di GitHub dan buat yang baru.
- Repo GitHub Pages gratis harus *public*, jadi isi `data.json` bisa dibaca siapa saja.
