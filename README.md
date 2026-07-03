# 📊 Catatan Scalping — Broker Flow Logger

Aplikasi web sederhana (single-file HTML) untuk mencatat dan memantau **broker flow** saham secara manual saat scalping/trading intraday di bursa saham Indonesia (IDX). Tidak perlu instalasi, tidak perlu server — tinggal buka file `.html` di browser.

## ✨ Fitur

- **Input cepat per saham**: kode saham, AVG (harga rata-rata), Slot (lot beli), dan Blot (lot jual)
- **Δ (Delta) otomatis**: menghitung perubahan Slot dan Blot dibanding entri sebelumnya untuk kode saham yang sama
- **Kolom Selisih**: selisih antara Blot dan Slot, dengan pewarnaan otomatis (hijau = positif, merah = negatif)
- **AVG berwarna dinamis**: AVG berwarna hijau jika naik, merah jika turun dibanding entri sebelumnya — memudahkan membaca arah average price secara sekilas
- **Filter per kode saham**: klik chip kode saham untuk fokus melihat flow satu ticker saja
- **Ringkasan (summary badges)**: total entri, total ΔSlot, total ΔBlot, dan selisih terakhir per kode/keseluruhan
- **Hapus baris atau hapus semua data** dengan satu klik
- Tampilan **dark mode** yang nyaman untuk dipakai saat market jam sibuk

## 🖥️ Cara Pakai

1. Download file `Catatan_Scalping.html`
2. Buka file tersebut langsung di browser (Chrome/Edge/Firefox — desktop maupun mobile)
3. Isi form **Input Data**:
   - **Kode Saham** — contoh: `RATU`
   - **AVG** — harga rata-rata broker saat itu
   - **Slot** — jumlah lot di sisi beli
   - **Blot** — jumlah lot di sisi jual
4. Klik **+ Tambah Entri**
5. Ulangi setiap kali ada update data broker flow — aplikasi otomatis menghitung Δ Slot, Δ Blot, dan Selisih dibanding entri sebelumnya untuk kode saham yang sama
6. Gunakan chip kode saham di atas tabel untuk memfilter tampilan per ticker

## ⚠️ Catatan Penting

- **Data tidak tersimpan permanen.** Aplikasi ini murni berjalan di memori browser (tidak memakai `localStorage`), sehingga semua data akan **hilang jika halaman di-refresh atau ditutup**. Cocok dipakai sebagai catatan cepat selama sesi trading berlangsung, bukan sebagai jurnal jangka panjang.
- Aplikasi ini adalah alat bantu pencatatan manual, **bukan alat analisis otomatis atau sinyal beli/jual**. Interpretasi data broker flow tetap menjadi tanggung jawab pengguna.
- Tidak ada koneksi ke data pasar real-time — semua angka diinput manual oleh pengguna.

## 🛠️ Teknologi

Dibangun murni dengan **HTML, CSS, dan Vanilla JavaScript** dalam satu file — tanpa dependency eksternal, tanpa build process, tanpa framework.

## 📌 Rencana Pengembangan (Ide)

- [ ] Penyimpanan data lokal (localStorage) agar data tidak hilang saat refresh
- [ ] Ekspor data ke CSV/Excel untuk dokumentasi jurnal trading
- [ ] Riwayat per hari/sesi trading

## 📄 Lisensi

Proyek pribadi untuk keperluan pencatatan trading sendiri. Bebas digunakan dan dimodifikasi.

---
*Dibuat untuk mempermudah pencatatan broker flow saat scalping saham di IDX.*
