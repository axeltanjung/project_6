### Project 6 - Fraud Detection menggunakan Apache Kafka

Proyek ini bertujuan untuk mendeteksi kecurangan dalam transaksi keuangan menggunakan Kafka sebagai platform streaming dan pemrosesan data.

Deskripsi
Proyek ini menggunakan Kafka untuk menerima data transaksi keuangan secara real-time, menganalisis pola dan anomali dalam data transaksi tersebut, dan memberikan notifikasi atau tindakan deteksi kecurangan jika diperlukan.

Fitur
Menerima data transaksi secara real-time melalui Kafka Producer.
Menganalisis pola dan anomali dalam data transaksi dengan Kafka Streams.
Mendeteksi potensi kecurangan berdasarkan pola yang tidak biasa atau anomali dalam data.
Mengirim notifikasi atau tindakan deteksi kecurangan melalui Kafka Consumer.
Arsitektur
Arsitektur proyek ini terdiri dari tiga komponen utama:

Kafka Producer: Komponen ini bertugas untuk mengirim data transaksi ke Kafka topic.
Kafka Streams: Komponen ini melakukan analisis data transaksi untuk mendeteksi kecurangan.
Kafka Consumer: Komponen ini menerima notifikasi atau tindakan deteksi kecurangan dari Kafka topic.
Penggunaan
Pastikan Anda memiliki Apache Kafka terpasang dan berjalan.
Jalankan Kafka Producer untuk mengirim data transaksi ke Kafka topic.
Jalankan Kafka Streams untuk menganalisis data transaksi dan mendeteksi kecurangan.
Jalankan Kafka Consumer untuk menerima notifikasi atau tindakan deteksi kecurangan.
