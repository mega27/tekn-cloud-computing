Cassandra Query Language (CQL)
Cassandra Query Language atau CQL adalah bahasa deklaratif yang memungkinkan pengguna untuk meminta Cassandra menggunakan bahasa yang mirip dengan SQL. CQL diperkenalkan di Cassandra versi 0.8 dan sekarang merupakan cara yang lebih disukai untuk mengambil data dari Cassandra. Sebelum pengenalan CQL, Thrift API berbasis RPC, adalah cara yang disukai untuk mengambil data dari Cassandra. Manfaat utama CQL adalah kesamaannya dengan SQL dan karenanya membantu menurunkan kurva pembelajaran Cassandra. CQL adalah SQL dikurangi bit yang rumit. Pikirkan CQL sebagai API sederhana di atas struktur penyimpanan internal Cassandra.

Dasar-dasar CQL
Mari kita memahami beberapa konstruksi CQL dasar sebelum kita beralih ke contoh praktis.

Keyspace - Keyspace mirip dengan basis data RDBMS. Ini adalah wadah untuk data aplikasi Anda. Seperti halnya database, suatu keyspace harus memiliki nama dan atribut yang terkait. Dua atribut penting yang harus ditetapkan ketika mendefinisikan ruang kunci adalah faktor replikasi dan strategi replikasi.

Keluarga / Tabel Kolom - Keluarga / tabel kolom mirip dengan tabel RDBMS. Ruang kunci terdiri dari sejumlah Keluarga / Tabel Kolom. Untuk sisa artikel ini, saya akan merujuk pada keluarga kolom / tabel secara bergantian.

Kunci Utama / Tabel - Kunci utama memungkinkan pengguna mengidentifikasi secara unik "baris internal" data. Kunci utama terdiri dari dua bagian. Kunci baris / partisi dan kunci cluster. Kunci baris / partisi menentukan node tempat data disimpan sementara kunci kluster menentukan urutan data di dalam baris tertentu.