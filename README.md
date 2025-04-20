#### Nama : Zakiah Rahmah Arrindani
#### NIM : 09011382429151
#### Kelas : SKU2A 


# PIPELINE PROCESSING 

## Pengertian Pipeline Processing
Dalam komputer, pipeline adalah satu set dari elemen pemrosesan data dihubungkan secara seri, sehingga hasil keluaran dari satu elemen adalah masukkan bagi elemen berikutnya. Elemen - elemen dari sebuah pipeline sering dijalankan secara paralel.
Contoh pipeline dalam komputer adalah:
- pipeline instruksi. Biasanya digunakan di unit pemroses sentral agar instruksi - instruksi dapat dijalankan dalam satu waktu dalam satu sirkuit digital. Biasanya sirkuitnya dibagi dalam beberapa tahap, termasuk decode instruksi, aritmetika dan tahap - tahap penjemputan data dari register, dimana setiap tahap melakukan satu instruksi dalam satu waktu.
- pipeline grafis, sering ditemukan dalam sebagian besar unit pemrosesan grafis, yang terdiri dari berbagai unit aritmatik atau unit pemroses sentral lengkap, yang menerapkan berbagai macam tahap dari operasi render yang umum (seperti proyeksi perspektif, kalkulasi warna dan pencahayaan, primitif gambar, dan sebagainya).
pipeline perangkat lunak. Dimana keluaran dari suatu program langsung dipakai oleh program lain sebagai masukkan sehingga dapat langsung diproses.

## Instruksi pipeline

Tahapan pipeline antara lain :
1.Mengambil instruksi dan membuffferkannya
2. Ketika tahapan kedua bebas tahapan pertama mengirimkan instruksi yang dibufferkan tersebut .
4. Pada saat tahapan kedua sedang mengeksekusi instruksi, tahapan pertama memanfaatkan siklus memori yang tidak dipakai untuk mengambil dan membuffferkan instruksi berikutnya .
Instuksi pipeline:

Karena untuk setiap tahap pengerjaan instruksi, komponen yang bekerja berbeda, maka dimungkinkan untuk mengisi kekosongan kerja di komponen tersebut.Sebagai contoh :
Instruksi 1: ADD  AX, AX
Instruksi 2: ADD EX, CX
Setelah CU menjemput instruksi 1 dari memori (IF), CU akan menerjemahkan instruksi tersebut(ID). Pada menerjemahkan instruksi  1 tersebut, komponen IF tidak bekerja. Adanya teknologi pipeline menyebabkan IF akan menjemput instruksi 2 pada saat ID menerjemahkan instruksi 1. Demikian seterusnya pada saat CU menjalankan instruksi 1 (EX), instruksi 2 diterjemahkan (ID).

## Contoh Kasus Pipeline Processing

Salah satu penerapan pipeline processing yang umum digunakan dalam sistem keamanan cerdas adalah deteksi dan pengenalan wajah secara real-time melalui video streaming dari kamera pengawas di area bandara. Proses ini dimulai dengan akuisisi data berupa aliran video dari kamera IP, yang kemudian dipecah menjadi frame-frame individual dengan interval waktu tertentu. Setiap frame selanjutnya diproses melalui tahapan pra-pemrosesan, seperti penyesuaian ukuran (resize), konversi warna (jika diperlukan), serta normalisasi nilai piksel guna memastikan kompatibilitas dengan model pembelajaran mesin yang digunakan. Setelah tahap ini, sistem melakukan deteksi wajah menggunakan algoritma berbasis convolutional neural networks (CNN), seperti Multi-task Cascaded Convolutional Networks (MTCNN) atau You Only Look Once (YOLO), untuk mengidentifikasi dan menandai posisi wajah pada setiap frame. Wajah-wajah yang terdeteksi kemudian dianalisis lebih lanjut melalui modul pengenalan wajah (face recognition), yang menggunakan teknik ekstraksi fitur dan representasi embedding—misalnya dengan menggunakan model FaceNet—untuk mencocokkan hasil deteksi dengan data identitas yang tersimpan dalam basis data internal. Apabila sistem tidak menemukan kecocokan, individu tersebut diklasifikasikan sebagai tidak dikenal dan ditandai sebagai potensi ancaman. Hasil analisis ini akan diteruskan ke sistem pencatatan dan pemberitahuan, yang bertugas menyimpan log aktivitas serta mengirimkan peringatan kepada petugas keamanan jika terdeteksi adanya aktivitas mencurigakan di area terbatas. Pipeline ini memungkinkan pemrosesan data yang bersifat sekuensial dan efisien, serta mendukung pengambilan keputusan secara cepat dan akurat dalam lingkungan yang menuntut respons waktu nyata (real-time).

