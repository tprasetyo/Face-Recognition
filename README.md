# Project 1 : Face Recognition
Face Recognition merupakan Project ke-1 dari Indonesia.AI dalam menyelesaikan Bootcamp Computer Vision Specialist.

#### Author : Teguh Prasetyo

## Pendahuluan
Teknologi Artificial Intelligence (AI) dewasa ini sangat bermanfaat bagi masyarakat. Salah satu bidang AI yang banyak diaplikasikan dalam kehidupan sehari-hari yaitu Computer Vision, dimana computer dilatih untuk dapat mengenali image (citra). Misalnya Face Recognition, dimana computer dilatih untuk dapat membedakan wajah laki-laki atau perempuan, atau lebih jauh lagi dapat mengenali nama seseorang dari wajahnya. Face Recognition ini sangat bermanfaat dalam kehidupan sehari-hari, misalnya untuk absensi kehadiran di suatu kantor, untuk tujuan authentifikasi pemilik akun/ID dan lain-lain seperti pada foto di bawah ini.

![mesin-pengenalan-wajah](https://github.com/tprasetyo/Face-Recognition/assets/72024376/d1deed43-d1e5-4ee6-9509-406d77a08b82)

## Objektif

Project ini bertujuan untuk melakukan eksperimen dengan 3 algoritma Deep Learning populer yaitu VGG, GoogleNet dan ResNet dan mengoptimalkan penggunaannya dengan melakukan hyperparameter tuning. Kemudian dari hasil eksperimen tersebut akan dilakukan pengambilan kesimpulan algoritma terbaik.

## Dataset

Image dataset yang digunakan dalam project ini terdiri dari 5000 images (terdapat 17 image duplikat). List nama file dari setiap image yang digunakan dapat dilihat pada file dengan nama  `List Nama File Foto sebagai Dataset.csv`, untuk mendapat file image tersebut dapat mendownload dari [CelebA](https://mmlab.ie.cuhk.edu.hk/projects/CelebA.html) di Kaggle, kemudian filter image sesuai List nama file yang ada pada file CSV tersebut. Untuk menentukan kategori Gender Male atau Female dapat menggunakan file `list_attribute.csv` pada kolom *image_id* dan kolom *Male*, kemudian lakukan *Join Inner* pada kolom *image_id* antara file *List Nama File Foto sebagai Dataset.csv* dengan *list_attribute.csv*, sehingga diperoleh 5000 baris data yang sama dengan dataset Image.  

## Metodologi

Training model deep learning menggunakan library keras dan tensorflow. Lebih detail dapat dilihat pada notebook.

Dalam proses penyelesaian tugas eksperimen dibuat bertahap, sehingga tahapannya membuat eksperimen dengan VGG-19 dahulu melalui eksperimen 1, 2 dan 3. Hasil terbaik dari eksperimen dengan VGG-19 tersebut kemudian di gunakan Model parameternya untuk pengerjaan dengan algoritma ResNet-50 dan GoogleNet (Inception-V3) untuk perbandingan.

Berikut List Filenya :

VGG-19 
* Eksperimen 1 : nama file -> Face Recognition tf vgg epoch 10 Exp 1 @ Teguh.ipynb
* Eksperimen 2 : nama file -> Face Recognition tf vgg epoch 10 Exp 2 @ Teguh.ipynb
* Eksperimen 3 : nama file -> Face Recognition tf vgg epoch 20 Exp 3 @ Teguh.ipynb

Pada eksperimen menggunakan VGG-19, hasil terbaik adalah pada Eksperimen 2, sehingga untuk algoritma ResNet dan GoogleNet menggunakan parameter yang sama dengan VGG-19 eksperimen 2.

ResNet-50
* Eksperimen 2 : nama file -> Face Recognition tf resnet epoch 10 Exp 2 @ Teguh.ipynb

GoogleNet (Inception-V3)
* Eksperimen 2 : nama file -> Face Recognition tf inceptionv3 epoch 10 Exp 2 @ Teguh.ipynb

## Hasil

![Perbandingan Algoritma VGG-Resnet-Googlenet](https://github.com/tprasetyo/Face-Recognition/assets/72024376/71327b82-49f9-47e8-8088-ae61dc0706f3)

Hasil terbaik adalah dengan menggunakan algoritma ResNet-50 dengan accuracy 0.95.

Catatan: Training menggunakan CPU dengan IDE VSCode 

## Kesimpulan

* Penggunaan Transfer Learning pada task Gender Classification dapat memberikan hasil akurasi yang tinggi 
* Tuning parameter seperti jumlah dense layer, fine tuning, loss function, dll bisa memiliki pengaruh terhadap hasil akurasi
* Transfer Learning bisa mendapatkan akurasi yang cukup baik walaupun hanya menggunakan data yang lebih sedikit.

## Contact

Teguh Prasetyo
  * Email : teguh.prasetyo33@gmail.com
  * Linkedin : https://id.linkedin.com/in/teguh-prasetyo-b4196879
  * RPubs : https://rpubs.com/tprasetyo

