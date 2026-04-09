## Ringkasan Proyek

Dalam implementasi halaman produk barang pada `3_ConstraintLayoutApp`, kerumitan
tata bahasa grafis ditempuh menggunakan kanon pamungkas, yaitu `ConstraintLayout`.
Karena arsitekturnya difokuskan membentangkan letak tanpa perdebatan dalam bersarang
(*nested linear tree*), elemen label promosi, deskripsi puitis toko, maupun
papan menu tombol "Beli" dikerek selaras satu padu menggunakan koneksi tali
magnetik (contohnya `app:layout_constraintTop_toBottomOf`). Kepingan antar harga
dan selektor angka ditata melar responsif menghalangi pemborosan ruang mati.

## Dokumentasi Teknis

### 1. Penjelasan File Resource Pendukung

Kanvas sekeras layar detail dagangan sangat terikat pada asupan eksternal folder
gambar (termasuk *drawable* sirkular `bg_circle_white.xml` beserta corak kapsul
`bg_btn_sage_green.xml`).

-   **Fungsinya:** Kode gambar merias ujung tumpul tombol harga serta merangkul
    ikon tanda silang / kembali di sisi atas rupa layar dengan latar semi transparan.
-   **Mengapa dipisah?:** Pemrograman Android menjauhkan diri dari penanaman nilai
    titik kelengkungan sudut (`radius`) pada badan *file* tata letak kasar
    `activity_main.xml`. Jika dipaksakan, barisan perintah tersebut merobek
    kerapihan struktural kode utama. Berkas `.xml` fungsional khusus digiring 
    menempati ruang repositori bentuk senkritis / res.

### 2. Penjelasan Logika Layout Utama (`activity_main.xml`)

Keagungan **ConstraintLayout** bukan bertahta di perletakan datar, melainkan 
keilmuan tegangan tarik tambang (ikatan sumbu titik nol antar gawang elemen). 

-   **`app:layout_constraintTop_toBottomOf="..."`**: Atribut nyawa pengikat ini 
    merengkuh dan mengekang langit (*Top*) komponen terpilih untuk ditancapkan 
    mutlak persis mencium leher belakang (*Bottom*) elemen idolanya di atas tadi. 
-   **Rentang Ruang Nostalgia (`0dp`)**: Di benak letak Constraint, dimensi `0dp`
    mustahil merujuk pada ukuran hampa ketiadaan. Benda itu dikutuk merenggang
    melar bak permen karet (*match constraint*) menyeimbangkan bujur kosong antara
    kedua sisi simpulnya.
-   **Elevasi Ruang (*elevation*)**: Digunakan menumbuhkan bayang jatuh (efek semu 
    hologram *Shadow*) agar Bar Pembelian Bawah terasa lebih "mewah" membaur tak
    terbanting rata bertindih di satu ubin kanvas yang sama.

### 3. Alur Visual

Sistem jalinan tali tambang maya menaklukkan interaksi silang elemen visual:

1.  **Lapis Kubah Paralel**: Bingkai ini dibelah secara makro atas tubuh kanvas 
    pembawa ulasan menggulung (`ScrollView`) di paruh rongga dada ke atas, 
    berseberangan letak membatu pada Balok Alas Belanja di pergelangan *Bottom Bar*.
2.  **Terjun Bebas Galeri**: Lukisan pajangan (*Image Penuh*) terpampang di dinding. 
    Ajaibnya, sepasang lingkar pelampung (*Back Arrow* & *Love Icon*) ditalikan 
    tahan mengambang murni di bingkai langit, tak tersentuh sistem antrean paragraf.
3.  **Tusukan Monumen Judul**: Kolom lembar keterangan harga dan reputasi 
    bintang mencubit garis margin terbalik untuk menyodok perut fotogenik gambar, 
    melindungi ruang peralihan antar pigura agar terlihat bertingkat presisi.
4.  **Batas Parit Pembayaran**: Penuh atau sebentar layar pengguna menjelajahi ulasan, 
    benteng gembok kuantitas dan label hijau *Beli* merantai diri enggan terusik, 
    menahan laju guling selimut di pinggiran dasar alas secara utuh menawan.
