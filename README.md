# Aquanice – Les Renang

Situs statis untuk GitHub Pages. Isi situs ada di `data.json` dan folder `images/`, tampilannya di `index.html`.

## Pasang di GitHub Pages
1. Buat repositori baru di GitHub (misalnya `aquanice`), lalu unggah semua isi folder ini (termasuk folder `images` dan file `.nojekyll`).
2. Buka **Settings → Pages**. Pada *Build and deployment* pilih **Deploy from a branch**, branch `main`, folder `/ (root)`, lalu **Save**.
3. Tunggu satu sampai dua menit. Alamat situs muncul di halaman Pages itu.

## Mengubah isi lewat panel admin
1. Buka situs, klik **Admin** di bagian paling bawah, lalu masukkan password.
2. Di GitHub buat token: **Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**. Pada *Repository access* pilih hanya repositori situs ini. Pada *Permissions → Repository permissions* set **Contents** ke **Read and write**.
3. Di panel admin buka tab **GitHub**, isi pemilik dan nama repositori (terisi otomatis bila alamat situs berakhiran `github.io`), tempel token, klik **Simpan token**, lalu **Uji koneksi**. Token hanya tersimpan di browser perangkat itu.
4. Ubah isi apa saja, lalu klik **Terbitkan perubahan**. Perubahan menjadi commit di repositori dan situs diperbarui sekitar 1 menit kemudian.

## Password admin
Password awal dibuat sebelum file ini dikirim, dan tidak tertulis di kode. Yang tersimpan hanya hash di `data.json`. Ganti lewat panel admin, tab **Keamanan**.
Password ini hanya pintu antarmuka, karena `data.json` bisa dibaca publik. Pengaman yang sebenarnya adalah token GitHub: tanpa token yang punya izin tulis, tidak ada yang bisa mengubah isi situs.

## Mencoba di komputer
File harus dilayani lewat server, bukan dibuka dengan klik dua kali. Jalankan `python3 -m http.server 8000` di folder ini, lalu buka http://localhost:8000.
