### Project 6 - Fraud Detection menggunakan Apache Kafka

Proyek ini bertujuan untuk mendeteksi kecurangan dalam transaksi keuangan menggunakan Kafka sebagai platform streaming dan pemrosesan data.

Deskripsi
Proyek ini menggunakan Kafka untuk menerima data transaksi keuangan secara real-time, menganalisis pola dan anomali dalam data transaksi tersebut, dan memberikan notifikasi atau tindakan deteksi kecurangan jika diperlukan.

Fitur
- Menerima data transaksi secara real-time melalui Kafka Producer.
- Menganalisis pola dan anomali dalam data transaksi dengan Kafka Streams.
- Mendeteksi potensi kecurangan berdasarkan pola yang tidak biasa atau anomali dalam data.
- Mengirim notifikasi atau tindakan deteksi kecurangan melalui Kafka Consumer.

Arsitektur
Arsitektur proyek ini terdiri dari tiga komponen utama:

- Kafka Producer: Komponen ini bertugas untuk mengirim data transaksi ke Kafka topic.
  Kafka Producer adalah komponen yang bertanggung jawab untuk mengirim data ke topik (topic) Kafka. Sebuah aplikasi atau sistem eksternal dapat bertindak sebagai Kafka Producer, menghasilkan data dalam bentuk pesan, dan mengirimkannya ke broker Kafka. Beberapa poin penting terkait dengan Kafka Producer adalah:

Mengirim Pesan: Producer mengirim pesan ke topik Kafka. Pesan ini dapat berupa data apapun, seperti log, metrik, atau transaksi keuangan.

Skema Data: Terkadang, penting untuk menentukan skema data yang diterima oleh Kafka Producer agar data dapat diinterpretasikan dengan benar oleh Kafka Consumer. Ini membantu dalam pemahaman struktur data yang dikirim dan menghindari kesalahan dalam pengolahan data.

Partisi: Kafka membagi topik menjadi partisi-partisi, yang merupakan unit penyimpanan data terdistribusi. Kafka Producer memutuskan ke partisi mana suatu pesan akan dikirim berdasarkan aturan tertentu. Biasanya, aturan ini dapat berupa algoritma round-robin, hash, atau aturan kustom yang diterapkan oleh pengembang.

Acknowledge: Kafka Producer mendukung konfirmasi (acknowledge) dari broker setelah pesan berhasil dikirim. Produser dapat mengonfigurasi level konsistensi untuk menentukan kapan pesan dianggap berhasil dikirim.


- Kafka Consumer: Komponen ini menerima notifikasi atau tindakan deteksi kecurangan dari Kafka topic.
Kafka Consumer adalah komponen yang bertanggung jawab untuk membaca data dari topik Kafka. Consumer dapat mengonsumsi data dalam berbagai cara, seperti memproses data secara real-time atau menyimpan data untuk analisis lebih lanjut. Beberapa aspek penting terkait dengan Kafka Consumer adalah:

Konsumsi Grup: Consumer biasanya bergabung dengan sebuah grup (group) untuk mengonsumsi data dari topik. Setiap grup dapat memiliki satu atau lebih consumer, dan setiap pesan di topik biasanya dikonsumsi oleh satu consumer dalam grup tersebut. Ini memungkinkan skalabilitas horizontal dan keandalan, karena beberapa instance consumer dapat membaca data dari topik yang sama.

Offset: Kafka menggunakan konsep offset untuk melacak kemajuan konsumsi data oleh setiap consumer. Offset adalah posisi terakhir yang dikonsumsi oleh consumer dalam topik. Dengan menggunakan offset, Kafka Consumer dapat mengambil data yang belum dikonsumsi setelah pemulihan atau restart.

Pengolahan Data: Consumer dapat mengolah data yang dikonsumsi dari topik sesuai dengan kebutuhan aplikasi. Ini bisa termasuk pemrosesan data real-time, analisis, penyimpanan ke database, atau pengiriman notifikasi.

Commit Offset: Kafka Consumer dapat mengonfirmasi offset kepada broker setelah berhasil mengkonsumsi pesan. Ini memastikan bahwa data tidak akan hilang saat consumer mengalami kegagalan atau restart.

Penggunaan
- Pastikan Anda memiliki Apache Kafka terpasang dan berjalan.
- Jalankan Kafka Producer untuk mengirim data transaksi ke Kafka topic.
- Jalankan Kafka Streams untuk menganalisis data transaksi dan mendeteksi kecurangan.
- Jalankan Kafka Consumer untuk menerima notifikasi atau tindakan deteksi kecurangan.
