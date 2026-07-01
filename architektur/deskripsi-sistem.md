# Deskripsi sistem akademik kampus
Nama Sistem: Sistem Informasi Integrasi Berbasis Akademik

Tujuan Sistem:
SiberAkad dirancang untuk mendigitalisasi, mengintegrasikan, dan mengotomatisasi seluruh siklus layanan administrasi akademik kampus. Sistem ini bertujuan untuk meningkatkan efisiensi kerja staf administrasi, transparansi proses akademik bagi dosen, serta memberikan kemudahan akses informasi bagi mahasiswa secara real-time, aman, dan responsif (bahkan dalam kondisi lonjakan trafik tinggi seperti saat pengisian KRS).

Pengguna Utama 
Sistem ini mengadopsi konsep Role-Based Access Control (RBAC), di mana setiap pengguna memiliki hak akses yang berbeda sesuai fungsinya:
Mahasiswa: Pengguna akhir yang mengonsumsi layanan akademik (KRS, melihat nilai, presensi, pengajuan cuti/sidang).

Dosen (Dosen Pengajar & Dosen Wali): Pengguna yang melakukan input nilai, melakukan presensi kuliah, dan menyetujui rencana studi mahasiswa bimbingannya.

Administrator Akademik: Operator pusat yang mengelola master data (jadwal kuliah, kurikulum, ploting dosen, ruang kelas, dan batas waktu kalender akademik).

Bagian Keuangan: Pengolah data pembayaran kuliah (UKT/SPP) yang terintegrasi dengan sistem bank.

Pimpinan Kampus (Rektor/Dekan/Kaprodi): Memantau laporan eksekutif statistik IPK, kelulusan, dan kinerja dosen melalui dashboard analitik untuk melihat proges mahasiswa.

Fitur-Fitur Utama:
Sistem Informasi Integrasi Berbasis Akademik dibagi menjadi beberapa modul utama yang saling terhubung:
1. Modul KRS Online
KRS War Handling: Fitur pengisian Kartu Rencana Studi (KRS) online yang dilengkapi sistem antrean agar server tidak tumbang saat diakses ribuan mahasiswa serentak.
Prerequisite Checking: Validasi otomatis sistem terhadap syarat matakuliah misal: tidak bisa mengambil Skripsi jika belum lulus Metodologi Penelitian.
2. Modul Penjadwalan & Ruang Kelas
Smart Scheduling: Fitur ploting jadwal kuliah otomatis untuk meminimalisir bentrok jadwal dosen, mahasiswa, maupun penggunaan ruang kelas.
Kalender Akademik Dinamis: Pengaturan linimasa kampus mulai dari masa bayar kuliah, masa isi KRS, minggu perkuliahan, hingga input nilai UAS.
3. Modul Pembelajaran & Presensi (Perkuliahan)
Presensi Digital: Pencatatan absensi mahasiswa menggunakan QR Code atau input manual oleh dosen via aplikasi mobile.
Beban Kerja Dosen (BKD): Perekaman otomatis aktivitas mengajar dosen untuk kebutuhan pelaporan internal dan kementerian.
4. Modul Penilaian & Transkrip
Otomatisasi Komponen Nilai: Perhitungan otomatis nilai akhir berdasarkan bobot Tugas, UTS, UAS, dan Presensi sesuai kebijakan kampus.
Kunci Nilai (Locking System): Batas waktu otomatis bagi dosen untuk mengunci nilai agar tidak bisa diubah sepihak setelah dipublikasikan ke mahasiswa.
Transkrip Nilai Digital: Unduh KHS (Kartu Hasil Studi) dan Transkrip Nilai sementara berformat PDF resmi yang dilengkapi pengaman QR Code.
5. Modul Keuangan (Host-to-Host Integration)
Auto-Lock Clearance: Sistem otomatis mengunci akses KRS atau pengisian nilai bagi mahasiswa yang belum melunasi tagihan biaya kuliah (UKT).
Multi-Channel Payment: Integrasi dengan Virtual Account berbagai bank dan dompet digital, sehingga status pembayaran langsung terupdate saat itu juga (real-time).
6. Modul Tugas Akhir, Kelulusan, & PDDIKTI Sync
E-Bimbingan: Monitoring progres bimbingan skripsi/tugas akhir antara mahasiswa dan dosen pembimbing.
Yudisium & Wisuda Ready: Verifikasi otomatis kelayakan kelulusan berdasarkan jumlah SKS yang ditempuh, skor TOEFL, dan bebas pustaka/keuangan.

