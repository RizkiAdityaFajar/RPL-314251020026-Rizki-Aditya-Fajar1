# Logical view- Sistem akademik kampus

Hubungan dan Aliran Kerja Antar Modul
Setiap modul di dalam Business Logic Layer tidak berdiri sendiri, melainkan saling bertukar data untuk menjalankan proses akademik:

A. Authentication Module 
Hubungan ke UI: Menjadi filter pertama bagi semua User Interface. Sebelum pengguna bisa melihat menu, mereka wajib divalidasi oleh modul ini.
Hubungan ke Modul Lain: Setelah login berhasil, modul ini akan mengirimkan token akses berisi informasi Role apakah dia Mahasiswa atau Dosen ke modul-modul bisnis agar pengguna mendapatkan hak akses yang sesuai.
B. Academic Management Module 
Hubungan dengan Grading Module: Modul ini menyuplai data daftar mahasiswa yang sah mengambil suatu matakuliah peserta kelas ke Modul Penilaian. Tanpa data dari modul akademik, dosen tidak bisa menginput nilai.
Hubungan dengan Reporting Module: Menyediakan data mentah berupa status keaktifan mahasiswa, jumlah SKS yang diambil, dan jadwal kuliah untuk diolah menjadi laporan.
C. Grading Module (Modul Penilaian)
Hubungan dengan Academic Management Module: Setelah dosen mengunci nilai UAS, modul ini akan mengirimkan data nilai akhir kembali ke Modul Akademik untuk memperbarui status kelulusan matakuliah prasyarat dan menghitung Indeks Prestasi Semester.
Hubungan dengan Reporting Module: Menyuplai data nilai kumulatif untuk dicetak menjadi KHS (Kartu Hasil Studi) dan Transkrip Nilai.
D. Reporting Module (Modul Pelaporan)
Hubungan dengan Semua Modul Bisnis: Modul ini bersifat read-only hanya membaca. Ia menarik data dari Modul Akademik (historis kuliah) dan Modul Penilaian (IPK) untuk menyajikannya dalam bentuk grafik dashboard bagi Pimpinan atau diekspor ke format PDDIKTI.
E. Database Module (Penyimpanan Pusat)
Hubungan dengan Semua Modul: Berada di lapisan paling bawah. Semua modul bisnis (Akademik, Penilaian, Pelaporan) terhubung ke Database Module melalui Data Access Object untuk menyimpan,Update , atau mengambil data secara aman.