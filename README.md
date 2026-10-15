# Safari Bundar / Rounding Safari

Aplikasi dwibahasa oleh Cikgu A’liyah. Fail statik tanpa pemasangan, akaun, iklan atau kebergantungan internet. Haiwan dipaparkan menggunakan emoji peranti.

## Cuba sekarang
Ekstrak ZIP dan buka `index.html` dalam Chrome, Edge, Firefox atau Safari. Pastikan `style.css` dan `app.js` berada di folder yang sama.

## Kandungan
- Tahun 1: puluh; Tahun 2: hingga ratus; Tahun 3: hingga ribu; Tahun 4: hingga puluh ribu; Tahun 5: hingga ratus ribu; Tahun 6: hingga juta.
- Pembahagian nilai bundar mengikut skop yang ditetapkan oleh guru untuk aplikasi ini.
- Julat nombor yang dijana: Tahun 1 bawah 100, Tahun 2 bawah 1 000, Tahun 3 bawah 10 000, Tahun 4 bawah 100 000, Tahun 5 bawah 1 000 000, Tahun 6 bawah 10 000 000. Jawapan bundar boleh mencapai had atas.
- Praktis berpandu enam langkah yang boleh dilangkau. Murid memilih digit, mengenal digit penentu dan memilih tambah 0 atau 1.
- Senang: pilihan jawapan, panduan penjaga zoo beransur kurang.
- Sederhana: taip nombor tanpa penanda digit.
- Susah: taip nombor; sekurang-kurangnya lima soalan melibatkan pengumpulan semula.
- 10 soalan setiap pusingan. Markah satu bagi setiap jawapan betul. Jawapan tersalah diberi penerangan; tiada penalti masa.
- Mod campuran mengitar nilai bundar yang tersedia untuk tahun yang dipilih.
- Toggle bahasa mengekalkan kemajuan. Nama panggilan diminta untuk profil; kelas tidak diperlukan. Nama, koleksi dan permainan belum selesai disimpan dalam localStorage pada pelayar/peranti yang sama.

## Kaedah Cikgu
Kira sifar pada nilai bundar, bulatkan bilangan digit yang sama dari belakang, dan lihat digit paling kiri dalam kumpulan yang dibulatkan. Digit 0–4 ialah nombor miskin (tambah 0 kepada bahagian kiri); digit 5–9 ialah nombor kaya (tambah 1 kepada bahagian kiri). Gantikan semua digit yang dibulatkan dengan sifar. Menambah pada bahagian kiri turut mengendalikan pengumpulan semula, contohnya 395 menjadi 400.

## GitHub Pages (apabila bersedia)
1. Cipta repository GitHub.
2. Muat naik `index.html`, `style.css`, `app.js` dan README ini ke akar repository, bukan fail ZIP.
3. Buka Settings → Pages → Build and deployment → Deploy from a branch.
4. Pilih branch `main`, folder `/ (root)` dan Save.
5. Tunggu GitHub menyediakan pautan Pages.

Tiada deployment dilakukan dalam pakej ini. Semua laluan aset adalah relatif, sesuai untuk GitHub Pages dalam subfolder repository.

## Semakan
`node --check app.js` untuk sintaks. `node tests/check.cjs` untuk semakan penjana soalan, kes pengumpulan semula, skor dan aliran praktis. Semakan automatik bukan pengganti semakan visual pada peranti murid.

## Kemas kini interaksi
Praktis kini menggunakan satu ruang dengan penjaga zoo dan bubble panduan. Tiada butang Next untuk langkah praktis. Murid membulatkan digit sendiri, menaip jawapan, kemudian menekan Semak jawapan. Petunjuk mengenal pasti kesilapan bahagian kiri dan/atau digit hujung yang perlu menjadi sifar, tanpa menunjukkan jawapan penuh. Percubaan praktis tidak terhad.

Dalam permainan, tiada digit dibulatkan terlebih dahulu. Tahap senang memberi panduan penuh pada soalan 1–3, panduan ringkas pada 4–6, dan galakan sahaja pada 7–10. Murid boleh menekan digit untuk membuat bulatan sendiri. Kad nombor kaya/miskin tersedia pada tiga soalan pertama sahaja; kad sentiasa tersedia dalam praktis.

Setiap soalan permainan mempunyai dua percubaan. Kesilapan pertama memaparkan pop-up dwibahasa “Jawapan anda salah. Ada 1 kali percubaan lagi.” tanpa jawapan atau penerangan penyelesaian. Pilihan yang salah dinyahaktifkan. Selepas kesilapan kedua, soalan tamat dan penerangan boleh dilihat. Jawapan betul pada mana-mana percubaan mendapat satu markah. Markah maksimum 10.

Pop-up gaya SweetAlert menggunakan dialog terbina dalam yang berfungsi tanpa internet atau CDN.

## Tutorial bergerak, kad seret dan bunyi
Tutorial visual berulang menunjukkan bulatan dan pergerakan kad +0/+1. Boleh ditutup atau diulang tanpa butang Next. Tutorial memaparkan jawapan contoh selepas animasi; murid menulis sendiri jawapan latihan yang berbeza. Seret kad ke kotak di atas digit sebelah kiri kumpulan yang dibulatkan; aplikasi menyemak jenis kad serta tempatnya. Pilihan tekan kad kemudian tekan kotak tersedia untuk papan kekunci dan sentuhan.

Digit tersalah pilih mendapat tanda merah ✕ dan pop-up segera. Maklum balas betul/salah dalam praktis dan permainan disertai bunyi ting/teeet yang dijana secara setempat. Butang Bunyi membolehkan bunyi dimatikan. Pelayar memerlukan interaksi pengguna sebelum membenarkan audio; visual kekal tersedia jika audio tidak disokong. Tetapan bunyi kekal sepanjang sesi dan kembali aktif apabila halaman dimuat semula. Mod kurangkan gerakan peranti menggantikan animasi dengan gambaran statik.

## Contoh tutorial dan mod campuran
Contoh tutorial mempunyai nombor sendiri yang berbeza daripada nombor latihan. Selepas gerakan kad, contoh memaparkan hasil seperti 345 → 350. Butang contoh tutorial lain tersedia. Dalam mod campuran, tutorial bertukar automatik setiap 8 saat mengikut nilai bundar tahun yang dipilih; pertukaran contoh hanya mengemas kini ruang tutorial dan mengekalkan input murid. Contoh latihan baharu turut bergilir nilai bundar. Tanda merah pada digit yang tersalah pilih hilang selepas 1.8 saat.

## Bantuan ketika menjawab soalan
Senang: digit boleh dibulatkan sendiri dan kad +0/+1 tersedia pada kesemua 10 soalan. Sederhana: bulatan sendiri pada semua soalan; kad +0/+1 tersedia pada soalan 1–5 sahaja. Soalan 6–10 sederhana melatih congak tanpa kad. Susah: taip jawapan tanpa bulatan atau kad.

Digit tersalah dibulatkan dalam soalan senang/sederhana mencetuskan pop-up dan bunyi salah dengan tanda merah sementara. Kad yang salah jenis atau kedudukan juga diberi amaran. Bantuan ini tidak menggunakan dua percubaan jawapan akhir dan tidak menolak markah. Bulatan, kad dan mesej bantuan dikosongkan untuk setiap soalan baharu.

## Safari Saya dan profil
16 spesies dalam empat kategori ganjaran permainan (kategori ini bukan pengelasan saintifik): 0–3 Biasa, 4–6 Istimewa, 7–9 Rare, 10 Legenda. Setiap pusingan 10 soalan yang lengkap memberi satu haiwan, mengutamakan spesies belum dimiliki dalam kategori markah itu. Jika kategori sudah lengkap, bilangan haiwan sedia ada bertambah. Amaran bantuan tidak menjejaskan markah.

Nama panggilan dan koleksi disimpan secara setempat; nama sama memilih semula profil yang sama (tanpa kata laluan). Butang Tukar pemain membuka senarai profil. Sambung permainan memulihkan soalan, markah, percubaan yang telah digunakan dan jawapan yang ditaip. Markah terkumpul, rekod terbaik dan bilangan pusingan turut disimpan.

Simpanan terikat kepada pelayar, peranti dan alamat laman. Data daripada fail tempatan tidak berpindah automatik ke GitHub Pages. Gunakan Muat turun sandaran di Safari Saya dan Pulihkan sandaran untuk memindahkan profil ke pelayar/peranti lain. Pemulihan menambah profil yang ID-nya belum wujud, tanpa menggantikan profil sedia ada; permainan separuh jalan tidak diimport. Fail sandaran mengandungi nama serta koleksi. Memadam data laman/pelayar atau menutup sesi private browsing boleh memadam simpanan. Tiada akaun awan, pelayan atau penghantaran nama ke pihak lain.
