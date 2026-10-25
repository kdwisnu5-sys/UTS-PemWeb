# Cerdas Digital-Literasi digital
Website Edukasi Cerdas digital
SDG 4 dan SDG 16

#Anggota Kelompok
1. Komang Arlan Airlangga - 2515091135 - Index.html, style beranda, responsive hp
2. I Gusti Putu Marlo Ardika Yudha - 2515091139 - Etika.html. style etika, responsive tablet
3. Kadek Wisnu Variandika - 2515091037 - Keamanan.html, Hoax.html, style keamanan, style hoax, responsive destop 
4. Muhammad Iqbal Yudiansyah - 2515091075 - Panduan.html, style panduan, animasi style

#Halaman Website
Beranda	index.html	Memperkenalkan website dan menampilkan topik pembelajaran.
Edukasi keamanan digital	keamanan.html	Menjelaskan phishing, malware, dan cara menjaga keamanan digital.
Artikel cek hoaks	hoax.html	Membahas ciri ciri hoaks, dampaknya, dan cara melakukan cek fakta.
Etika digital	etika.html	Menjelaskan etika berkomunikasi, privasi, cyberbullying, dan hak cipta.
Panduan digital	panduan.html	Memberikan langkah praktis menjaga keamanan akun, privasi, dan perangkat.

#Teknologi
HTML5: digunakan untuk menyusun struktur halaman website menggunakan elemen seperti header, nav, main, section, article, dan footer.
CSS3: digunakan untuk mengatur warna, ukuran teks, jarak, latar belakang, border, dan animasi.
Flexbox: digunakan untuk mengatur posisi logo dan navigasi agar sejajar.
CSS Grid: digunakan untuk menyusun kartu topik pembelajaran dan artikel dalam beberapa kolom.
CSS Media Queries: digunakan untuk menyesuaikan tampilan website pada perangkat HP, tablet, dan desktop.

#Penjelasan Implementasi
A. Navigasi website
Navigasi menggunakan elemen HTML <nav> yang berada di dalam <escape><header></escape>. Tautan mengarah ke lima halaman website sehingga pengguna dapat berpindah halaman.
Contoh kode HTML:
<nav class="navbar">
    <h1>Cerdas <span>Digital</span></h1>
    <div class="navbar-laptop-tablet">
        <a href="index.html">Beranda</a>
        <a href="keamanan.html">Keamanan Digital</a>
        <a href="hoax.html">Cek Hoax</a>
        <a href="etika.html">Etika Digital</a>
        <a href="panduan.html">Panduan Digital</a>
    </div>
</nav>

Fungsinya adalah menyediakan menu untuk berpindah dari satu halaman ke halaman lainnya. Pada layar HP, navigasi desktop disembunyikan dan digantikan dengan menu yang menggunakan elemen <details> dan <summary>.
<details> adalah elemen HTML yang berfungsi sebagai wadah untuk konten yang bisa dibuka dan ditutup.
Contohnya:
<details>
    <summary>☰</summary>
    <a href="index.html">Beranda</a>
    <a href="keamanan.html">Keamanan Digital</a>
</details>
Ketika halaman dibuka, pengguna akan melihat simbol ☰. Setelah simbol tersebut diklik, menu Beranda dan Keamanan Digital akan muncul. Jika diklik lagi, menu akan tertutup.

2. Elemen <summary>
<summary> adalah elemen yang menjadi judul atau bagian yang diklik untuk membuka dan menutup <details>.
Contoh:
<summary>☰</summary>
Simbol ☰ berfungsi sebagai ikon menu atau hamburger menu. Ketika pengguna mengekliknya, isi di dalam <details> akan ditampilkan atau disembunyikan.

Contoh CSS:
.navbar {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.header {
    position: fixed;
    top: 18px;
    z-index: 1000;
}

display: flex menyusun logo dan menu dalam satu baris. justify-content: space-between memberi jarak di antara keduanya. Sementara itu, position: fixed membuat header tetap berada di posisi atas saat halaman digulir, dan z-index: 1000 membantu menempatkan header di atas elemen lain.

B. Layout halaman
Website menggunakan Flexbox dan CSS Grid untuk menyusun konten.
Contoh Flexbox pada halaman utama:
.section-beranda-1 {
    min-height: 85vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

Kode tersebut menempatkan konten di tengah secara horizontal dan vertikal. min-height: 85vh membuat bagian beranda memiliki tinggi minimum sebesar 85% dari tinggi viewport.

Contoh CSS Grid:
.grid-beranda {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 50px;
}
Kode ini menyusun empat kartu topik pembelajaran menjadi dua kolom dengan jarak 50 piksel. Kartu dibuat menggunakan elemen <escape><article></escape> agar setiap topik memiliki struktur konten tersendiri.

C. Responsive design
Website menggunakan CSS Media Queries untuk menyesuaikan tata letak berdasarkan lebar layar. Terdapat tiga pengaturan utama.
/* HP */
@media screen and (max-width: 600px) {
    .grid-beranda {
        grid-template-columns: 1fr;
    }
}

/* Tablet */
@media screen and (min-width: 601px)
and (max-width: 1024px) {
    .grid-beranda {
        gap: 25px;
    }
}

/* Desktop */
@media screen and (min-width: 1025px) {
    .header {
        left: 10%;
        width: 80%;
    }
}

Penjelasan:
- HP (maksimal 600 px): kartu pembelajaran disusun menjadi satu kolom agar mudah dibaca pada layar kecil. Navigasi desktop disembunyikan dan menu HP ditampilkan.
- Tablet (601–1024 px): jarak antarkartu diperkecil agar konten sesuai dengan lebar layar.
- Desktop (minimal 1025 px): header menggunakan lebar 80% dan posisi kiri 10% agar navigasi terlihat proporsional.
Selain itu, website menggunakan width: 90%, max-width, dan padding pada sejumlah bagian agar konten memiliki ruang yang cukup.

D. Animasi CSS
Beberapa judul, paragraf, dan kartu memiliki animasi masuk dari bawah.
Contoh kode:
@keyframes naik {
    from {
        opacity: 0;
        transform: translateY(30px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}
Animasi tersebut mengubah transparansi dari tidak terlihat menjadi terlihat, sekaligus menggerakkan elemen dari posisi 30 piksel di bawah menuju posisi normal.
Animasi diterapkan menggunakan properti seperti animation, animation-delay, dan opacity.

E. Struktur konten HTML
Website menggunakan elemen semantik HTML5 untuk membedakan bagian-bagian halaman.
Elemen	Fungsi
<header>	Menampung bagian kepala halaman dan navigasi.
<escape><nav></escape>	Menampung tautan navigasi.
<escape><main></escape>	Menampung konten utama halaman.
<escape><section></escape>	Mengelompokkan konten berdasarkan bagian atau topik.
<escape><article></escape>	Menampung konten mandiri, seperti kartu pembelajaran atau artikel.
<escape><footer></escape>	Menampilkan informasi penutup dan identitas proyek.

#Struktur Folder
uts/
index.html — halaman beranda
keamanan.html — halaman keamanan digital
hoax.html — halaman cek hoaks
etika.html — halaman etika digital
panduan.html — halaman panduan digital
style.css — pengaturan tampilan dan responsive design
dokumen/
background.png — gambar latar belakang beranda

Folder dokumen/ menyimpan aset gambar yang digunakan website. Nama file dan folder harus sesuai dengan lokasi yang dipanggil pada kode HTML agar gambar dapat ditampilkan dengan benar.
