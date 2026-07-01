# Architecture 
Berikut adalah pola dan gaya arsitektur utama yang paling tepat dan umum digunakan dalam membangun SIAKAD modern:
Layered Architecture
Meskipun menggunakan microservices, di dalam setiap layanan kecil tersebut biasanya tetap menerapkan pola Layered tradisional untuk merapikan struktur kode pemrograman.

Cara Kerja: Kode dibagi menjadi lapisan yang terstruktur:
Presentation Layer
Business Logic Layer (Service/Aturan akademik seperti syarat SKS)
Data Access Layer (Repository/Query ke database)

Mengapa Cocok untuk Kampus? Membuat kode program menjadi rapi, mudah dirawat (maintainable), dan mudah dipahami oleh tim developer kampus yang berganti-ganti.

Gaya ini memecah sistem akademik yang besar menjadi layanan-layanan kecil yang mandiri berdasarkan domain bisnisnya.

Cara Kerja: Modul KRS, Modul Keuangan (UKT), Modul Penilaian, dan Modul Absensi berjalan di server/container yang terpisah.

Isolasi Kegagalan: Jika modul KRS tumbang atau kelebihan beban saat "KRS War", dosen tetap bisa menginput nilai di modul penilaian, dan mahasiswa tetap bisa membayar UKT di modul keuangan.