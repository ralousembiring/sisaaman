# SisaAman — Vercel static prototype v1

Prototype SisaAman menggunakan HTML, CSS, dan JavaScript. Tidak membutuhkan PHP/MySQL untuk versi ini sehingga bisa dipasang sebagai situs statis di Vercel.

## File project
- `public/index.html` — aplikasi SisaAman.
- `vercel.json` — memberi tahu Vercel bahwa output situs berada di folder `public`.

## Data awal benar-benar kosong
Pengguna baru tidak mendapat transaksi, tagihan, target, atau wishlist contoh. Saldo awal dan target tabungan bulanan bernilai nol sampai pengguna mengisinya sendiri. Versi ini menggunakan storage key baru (`sisaaman_v2_empty_start`) sehingga data contoh dari prototipe lama tidak terbaca di versi ini; data lama pada key sebelumnya tidak dihapus.

## Deploy lewat GitHub ke Vercel
1. Ekstrak ZIP.
2. Buat repository GitHub baru, misalnya `sisaaman`.
3. Unggah struktur project apa adanya: folder `public` dan file `vercel.json` harus berada di root repository.
4. Di Vercel, pilih **Add New → Project**, lalu import repository tersebut.
5. Pilih Framework Preset **Other**. Tidak perlu build command atau environment variables. `vercel.json` mengatur output ke folder `public`.
6. Klik **Deploy**.

## Batasan penting
- Versi ini belum memiliki login, PHP, MySQL, atau sinkronisasi antarperangkat.
- Data dicatat di `localStorage` pada browser/perangkat masing-masing. Browser atau perangkat berbeda tidak berbagi data. Pengguna lain pada profil browser yang sama dapat melihat data lokal yang tersimpan di profil tersebut.
- Catatan dapat hilang bila penyimpanan browser dibersihkan. Gunakan fitur cadangan JSON secara berkala.
- Jangan gunakan untuk data keuangan sangat sensitif sebelum sistem akun, otorisasi, perlindungan data, dan backup server dirancang dengan benar.
