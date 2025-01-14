## **BUSINESS UNDERSTANDING**

**Context**  
Deposito merupakan produk perbankan di mana seseorang menyetor sejumlah uang ke dalam rekening untuk jangka waktu tertentu dengan tingkat bunga yang tetap. Setelah jangka waktu tersebut berakhir, uang tersebut bersama dengan bunga dapat ditarik.
Sebagai kompensasinya, nasabah akan diberikan bunga tetap sesuai dengan nominal uang yang disetorkan.

Namun demikian, sebagai badan usaha dengan produk keuangan dan nasabahnya masing-masing, bank tetap harus bersaing agar tidak kehilangan nasabah. Salah satu cara untuk mendapatkan pelanggan baru adalah dengan melakukan kampanye pemasaran.

Berikut adalah data dari hasil kampanye pemasaran bank yang dilakukan melalui panggilan telepon langsung untuk menaruh deposit berjangka. Untuk klien yang setuju untuk menaruh deposit, variabel target akan diisi dengan 'yes', jika tidak 'no'

Target :

0 : Tidak menaruh deposit

1 : Menaruh deposit

**Problem Statement**

Proses kampanye penawaran deposit memakan waktu dan biaya, jika bank menargetkan semua nasabah tanpa melakukan penyaringan terlebih dahulu, maka akan ada pemborosan dari segi waktu dan biaya. Bank ingin meningkatkan efisiensi proses kampanye dengan menargetkan ke calon nasabah yang memiliki potensi untuk menaruh deposit.


**Goals**

Berdasarkan permasalahan tersebut, bank ingin memiliki kemampuan untuk memprediksi kemungkinan kandidat nasabah untuk mau menaruh deposit atau tidak, sehingga dapat menargetkan kampanye pada kandidat yang memiliki potensial untuk menaruh deposit.

Dan juga, perusahaan ingin mengetahui kriteria apa saja yang berpengaruh pada kandidat nasabah yang sudah menaruh deposit dan yang tidak menaruh deposit. 

**Analytic Approach**

Kita akan menganalisis data untuk menemukan pola yang membedakan kandidat nasabah yang akan menaruh deposit atau tidak.

Kemudian, dilanjutkan dengan membangun model klasifikasi yang akan membantu bank untuk dapat memprediksi probabilitas seorang kandidat nasabah akan/ingin menaruh deposit atau tidak.

**Evaluation Metric**

Type 1 error : False Positive  
Konsekuensi: membuang waktu dan biaya kampanye untuk nasabah yang tidak berpotensial menaruh deposit

Type 2 error : False Negative  
Konsekuensi: kehilangan kandidat nasabah potensial

Berdasarkan konsekuensinya, maka sebisa mungkin akan dibuat model yang dapat mengurangi cost kampanye dari bank, tetapi tanpa membuat menjadi kurangnya kandidat nasabah potensial yang dicari oleh bank. Jadi kita ingin sebanyak mungkin prediksi kelas positif yang benar, dengan sesedikit mungkin prediksi false positive. Sehingga yang akan kita gunakan adalah F1 Score.

## **DATA UNDERSTANDING**
----

### Attribute Information

| Attribute | Data Type | Description |
| --- | --- | --- |
| age | Integer | Usia nasabah |
| job | String | Pekerjaan nasabah |
| balance | Integer | Saldo nasabah di rekening |
| housing | String | Apakah nasabah mempunyai pinjaman untuk pembelian rumah |
| loan | String | Apakah nasabah mempunyai pinjaman pribadi |
| contact | String | Jenis komunikasi yang digunakan |
| month | String | Bulan terakhir kali melakukan kontak pada tahun ini  |
| campaign | Integer | Jumlah kontak yang dilakukan selama kampanye untuk nasabah ini |
| pdays | Integer | jumlah hari yang berlalu setelah nasabah terakhir dihubungi dari kampanye sebelumnya. |
| poutcome | String | Hasil dari kampanye pemasaran sebelumnya |
| deposit | String | Apakah nasabah melakukan deposito |
