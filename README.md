# Si Gizi — Demo GitHub Pages

Prototipe web responsif untuk mendemonstrasikan UI/UX aplikasi deteksi dini stunting balita bagi kader Posyandu.

## Fitur demo
- Dashboard ringkasan dan akses cepat
- Daftar dan formulir data balita
- Formulir pencatatan antropometri
- Riwayat pengukuran dan grafik tren berat badan
- Layar Z-score WHO (status belum terintegrasi)
- Layar prediksi prospektif XGBoost (simulasi UI, bukan model)
- Laporan CSV
- Layout responsif untuk HP dan desktop
- Data contoh fiktif untuk demo

## Deploy gratis dengan GitHub Pages
1. Buat repository baru di GitHub, misalnya `si-gizi-demo`.
2. Upload semua file di folder ini ke **root** repository. Pastikan `index.html` ada langsung di root, bukan di subfolder.
3. Buka **Settings → Pages**.
4. Pada **Build and deployment**, pilih **Deploy from a branch**.
5. Pilih branch `main`, folder `/(root)`, lalu tekan **Save**.
6. Tunggu beberapa menit. GitHub akan menampilkan URL demo, biasanya:
   `https://USERNAME.github.io/si-gizi-demo/`

Jika nama repository adalah `USERNAME.github.io`, URL biasanya `https://USERNAME.github.io/`.

## Catatan data dan penelitian
- Demo ini adalah situs statis. Data disimpan di `localStorage` browser/perangkat yang sedang digunakan.
- Data tidak tersinkronisasi ke pengguna lain dan dapat hilang jika data situs/browser dihapus.
- Gunakan data fiktif. Jangan masukkan identitas atau pengukuran balita nyata.
- Perhitungan Z-score WHO belum diimplementasikan. Jangan menafsirkan grafik sebagai kurva standar WHO.
- Model XGBoost belum dilatih/diintegrasikan. Tidak ada prediksi risiko nyata yang dibuat.
- Ini prototipe web responsif, bukan APK Android native.
- Untuk produksi, diperlukan backend, autentikasi, kontrol akses, kebijakan privasi, backup, audit keamanan, dan validasi klinis/metodologis.

## Pengembangan lokal
Cukup buka `index.html` di browser. Untuk pengalaman yang lebih konsisten, jalankan server statis lokal, misalnya:
```bash
python -m http.server 8000
```
Lalu buka `http://localhost:8000`.
