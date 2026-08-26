# SaveMoney App Pro - Platform Manajemen Keuangan Pribadi Komprehensif

Aplikasi web manajemen keuangan pribadi super komprehensif (**"SaveMoney App Pro"**) berbasis framework **Django (Python)** dengan UI/UX modern, clean, dan intuitif kelas industri menggunakan **Tailwind CSS**, **Alpine.js**, **Lucide Icons**, dan visualisasi grafik interaktif **Chart.js**.

---

## 🌟 Modul & Fitur Utama

### 1. 💼 Ringkasan Multi-Wallet & Total Kekayaan Bersih (Net Worth)
- **Net Worth Master Card:** Kartu akumulasi total saldo seluruh dompet, bank, e-wallet, dan portofolio investasi secara real-time.
- **Grid Kartu Dompet Interaktif:** Visualisasi kartu dompet dengan nomor akun, saldo, tipe akun (Bank, Cash, E-Wallet, Investasi), tombol transfer instan, dan mutasi per dompet.
- **Transfer Antar Dompet:** Fitur transfer instan antar dompet yang secara otomatis mendebit saldo dompet asal dan mengkredit saldo dompet tujuan.

### 2. ⚡ Pencatatan Transaksi & Modal Universal
- Modal input serbaguna untuk 3 mode transaksi: **Pemasukan**, **Pengeluaran**, dan **Transfer Antar Dompet**.
- Picker tanggal manual dengan HTML5 Date Picker (`type="date"`).
- Pilihan Dompet Sumber, Dompet Tujuan (mode Transfer), Kategori, Nominal (Rupiah), dan Catatan.
- Otomasi pembaruan dan pengembalian (*revert*) saldo dompet saat transaksi dibuat, diubah, atau dihapus.

### 3. 📊 Visualisasi & Grafik Finansial Interaktif (Chart.js)
- **Grafik Tren Arus Kas:** Perbandingan pemasukan vs pengeluaran 6 bulan terakhir.
- **Grafik Distribusi Kategori:** Donut chart proporsi alokasi pengeluaran per kategori di bulan berjalan.
- **Grafik Alokasi Aset Dompet:** Donut chart perbandingan kepemilikan saldo di seluruh dompet dan rekening.

### 4. 🎯 Modul Target Tabungan (Savings Goals)
- Kartu target finansial lengkap dengan *Progress Bar* persentase visual.
- Estimasi sisa hari dan bulan pencapaian berdasarkan tenggat waktu target.
- **Alokasi Saldo Cepat:** Setor saldo langsung dari dompet ke target tabungan secara terintegrasi.
- Penandaan status target selesai atau buka kembali.

### 5. ⚠️ Modul Anggaran & Peringatan Dini (Category Budgeting & Alerts)
- Manajemen batas maksimal pengeluaran bulanan per kategori.
- Pemantauan real-time realisasi pengeluaran vs batas limit.
- **Indikator 3 Tingkat Status:**
  - 🟢 **Aman (<80%):** Indikator hijau emerald.
  - 🟡 **Peringatan (80% - 100%):** Indikator kuning/oranye (*Warning Alert*).
  - 🔴 **Overbudget (>100%):** Indikator merah menyala (*Danger Alert*).
- Fitur **Salin Anggaran Bulan Lalu** untuk kemudahan perencanaan bulanan.

### 6. 📅 Tampilan Kalender Keuangan (Financial Calendar View)
- Grid kalender bulanan interaktif (Senin s/d Minggu).
- Navigasi bulan sebelumnya dan bulan berikutnya.
- Indikator harian: badge hijau untuk total pemasukan dan badge merah untuk total pengeluaran di setiap tanggal.
- Akses langsung ke mutasi transaksi pada tanggal tertentu.

### 7. 🔁 Transaksi Berulang & Tagihan Rutin (Recurring Bills)
- Daftar pengeluaran & pemasukan rutin (Gaji, Tagihan PLN, Wifi Indihome, Netflix, Spotify, Sewa Kos).
- Indikator status jatuh tempo (*Hari ini*, *Sisa X hari*, *Lewat tempo*).
- Tombol **"Bayar / Bukukan Sekarang"** yang langsung memproses transaksi ke dompet dan memajukan tanggal jatuh tempo berikutnya sesuai frekuensi (Harian, Mingguan, Bulanan, Tahunan).

### 8. 📄 Laporan Ringkasan & Ekspor Data
- **Ekspor CSV / Excel:** Unduh riwayat transaksi terfilter dengan format UTF-8 BOM untuk kompatibilitas Microsoft Excel.
- **Laporan Ringkasan Cetak / PDF:** Tampilan laporan keuangan bulanan terstruktur yang siap dicetak langsung atau disimpan sebagai file **PDF** melalui browser.

### 9. 🎨 Desain UI/UX Modern & Dark Mode
- Tema elegan dengan Dark Mode & Light Mode switcher yang tersimpan di *localStorage*.
- *Fully Responsive* untuk kenyamanan akses di HP (Mobile View) maupun Desktop.

---

## 🚀 Cara Menjalankan Aplikasi

### 1. Masuk ke Direktori Proyek
```bash
cd "c:\Users\ardiansyah\Documents\uts 2022\TA BARU\money"
```

### 2. Aktifkan Virtual Environment
- **Windows (PowerShell):**
  ```powershell
  .\venv\Scripts\Activate.ps1
  ```
- **Windows (Command Prompt):**
  ```cmd
  .\venv\Scripts\activate.bat
  ```

### 3. Jalankan Migrasi & Seeding Data Sampel
```bash
python manage.py migrate
python manage.py seed_data
```

### 4. Jalankan Server Django
```bash
python manage.py runserver
```

Buka di browser:
- **Aplikasi SaveMoney Pro:** [http://127.0.0.1:8000/](http://127.0.0.1:8000/)
- **Django Admin:** [http://127.0.0.1:8000/admin/](http://127.0.0.1:8000/admin/)

---

## 🔑 Akun Superuser Bawaan (Django Admin)
- **Username:** `admin`
- **Password:** `admin123`

---

## 🧪 Menjalankan Automated Tests
```bash
python manage.py test
```
Semua 16 unit tests mencakup fungsionalitas model, transaksi saldo, transfer antar dompet, target tabungan, anggaran, tagihan berulang, dan ekspor.
