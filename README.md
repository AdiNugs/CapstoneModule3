# CapstoneModule3
Capstone Module 3 (Python Notebook) : Prediksi Nasabah Potensial untuk Produk Deposito Berjangka

## Latar Belakang 
Sebuah bank ingin meningkatkan efektivitas kampanye pemasaran (marketing campaign) mereka untuk produk deposito berjangka (term deposit). Selama ini, bank menghubungi banyak sekali nasabah, baik nasabah lama maupun baru, untuk menawarkan produk ini. Namun, pendekatan ini memakan biaya operasional yang besar (misalnya, waktu agen call center, biaya SMS/email blast) dan memiliki tingkat konversi yang belum optimal, karena banyak nasabah yang dihubungi ternyata tidak tertarik.

## Problem Statement
Biaya untuk menjalankan kampanye pemasaran menjadi tidak efisien ketika bank menargetkan semua nasabah tanpa melakukan penyaringan terlebih dahulu. Banyaknya sumber daya yang terbuang untuk menghubungi nasabah yang tidak potensial mengurangi profitabilitas kampanye. Bank ingin proses pemasaran ini menjadi lebih cerdas dan hemat biaya.

## Goals 
Berdasarkan permasalahan tersebut, tujuan utama proyek ini adalah:

Membangun sebuah model klasifikasi yang mampu memprediksi probabilitas seorang nasabah akan berlangganan deposito berjangka ('yes') atau tidak ('no'). Dengan model ini, bank dapat memfokuskan upaya pemasarannya hanya pada nasabah yang paling potensial.
Mengidentifikasi faktor-faktor kunci yang paling berpengaruh terhadap keputusan nasabah untuk berlangganan. Informasi ini dapat digunakan untuk merancang strategi penawaran yang lebih personal dan relevan di masa depan.
Catatan: Kita akan berasumsi (seperti contoh) bahwa sebelumnya bank mungkin memiliki sistem sederhana atau tidak memiliki model sama sekali. Tujuan kita adalah membangun model machine learning yang kinerjanya jauh lebih baik.

## Metric Evaluation
Type 1 error : False Positive

Penjelasan: Model memprediksi nasabah akan berlangganan ('yes'), padahal kenyataannya tidak. Konsekuensi: Bank membuang-buang sumber daya (waktu, biaya telepon/email) untuk menghubungi nasabah yang salah. Ini adalah kerugian biaya operasional.

Type 2 error : False Negative

Penjelasan: Model memprediksi nasabah tidak akan berlangganan ('no'), padahal kenyataannya dia mau. Konsekuensi: Bank kehilangan kesempatan untuk mendapatkan nasabah baru dan dana depositonya. Ini adalah kerugian pendapatan (opportunity loss).

Kehilangan seorang nasabah potensial (False Negative) umumnya jauh lebih merugikan daripada biaya untuk satu panggilan telepon (False Positive). Keuntungan dari satu deposito baru bisa menutupi biaya pemasaran untuk puluhan nasabah yang tidak tertarik.

Oleh karena itu, fokus utama kita adalah meminimalkan False Negative sebisa mungkin. Kita ingin menangkap sebanyak mungkin nasabah yang sebenarnya potensial. Metrik yang paling sesuai untuk tujuan ini adalah Recall.

Recall mengukur seberapa banyak dari total nasabah yang sebenarnya berlangganan, yang berhasil diprediksi dengan benar oleh model kita.
Meskipun begitu, kita tidak bisa mengabaikan False Positive sepenuhnya. Jika model terlalu banyak salah tebak (Precision rendah), kampanye tetap tidak akan efisien. Oleh karena itu, kita akan menggunakan Recall sebagai metrik utama, namun tetap memperhatikan F1-Score sebagai penyeimbang yang baik antara Recall dan Precision.
