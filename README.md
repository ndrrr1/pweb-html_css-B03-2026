# pweb-html_css-B03-2026
## REPORTING
Dikerjakan oleh: 
1. Ndaru Satria Tama (5027251124)
2. Daffa Rifqi As Shidiq (5027251038)
3. Farrel Muhammad Athasyah Enrizy (5027251100)

### Halaman Landing Page (`index.html` & `index.css`)

Kode HTML (`index.html`):
```
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ndaru Satria Tama | Portfolio</title>
    <link rel="stylesheet" href="css/index.css">
</head>
<body>
    <nav>
        <div class="nav-links">
            <a href="index.html">Home</a>
            <a href="about.html">About</a>
            <a href="projects.html">Projects</a>
            <a href="cv.html">CV</a>
        </div>
    </nav>

    <section class="hero">
        <div class="hero-text">
            <p class="intro-label">Hello, I'm</p>
            <h1>Ndaru <span class="accent">Satria Tama</span></h1>
            <h2>Web Developer & UI/UX Designer</h2>
            <p class="description">Creating modern digital experiences through creativity, technology, and user-centered design.</p>
            
            <div class="hero-buttons">
                <a class="btn" href="cv.html">View My CV</a>
                <a class="btn btn-light" href="projects.html">Projects</a>
            </div>
            
            <div class="stats">
                <span class="skill">5+ Projects</span>
                <span class="skill">3 Years Experience</span>
            </div>
        </div>
        <div class="hero-image">
            <img src="images/profile.jpeg" alt="Foto profil Ndaru Satria Tama">
        </div>
    </section>
</body>
</html>
```

Kode CSS (`index.css`):
```
:root { --dark: #101820; --cream: #f8f3eb; --accent: #ffae7a; --white: #ffffff; }
* { box-sizing: border-box; font-family: Arial, sans-serif; }
body { margin: 0; background: var(--cream); color: #222; }

nav { 
    position: sticky; 
    top: 0; 
    z-index: 10; 
    padding: 20px 8%; 
    display: flex; 
    justify-content: flex-end; 
    background: var(--dark); 
}
.nav-links a { position: relative; color: #fff; text-decoration: none; font-size: 14px; margin-left: 20px; }
.nav-links a::after { 
    content: ""; 
    position: absolute; 
    left: 0; 
    bottom: -8px; 
    width: 0; 
    height: 2px; 
    background: var(--accent); 
    transition: 0.3s;
}
.nav-links a:hover::after { width: 100%; }

.hero { 
    min-height: 90vh; 
    display: flex; 
    justify-content: space-between; 
    align-items: center; 
    padding: 8%; 
    background: var(--dark); 
    color: #fff; 
}
.hero-image img { width: 380px; height: 380px; border-radius: 40px; }

@media (max-width: 800px) {
    nav { justify-content: flex-start; }
    .hero { display: flex; flex-direction: column; align-items: flex-start; }
    .hero-image img { width: 260px; height: 260px; }
}
```
Penjelasan Landing Page:

Halaman ini bertindak sebagai titik masuk utama (beranda) yang memuat perkenalan singkat dan navigasi ke seluruh bagian situs web. Struktur visualnya dibangun menggunakan Flexbox (`display: flex`) untuk memisahkan teks pengantar di sisi kiri dan gambar profil di sisi kanan secara seimbang. Navigasi dibuat menempel di bagian atas layar (`position: sticky`) untuk memudahkan perpindahan halaman kapan saja.

### Halaman Creative CV (`cv.html` & `cv.css`)
Kode HTML (`cv.html`):
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CV | Information Technology Student</title>
    <link rel="stylesheet" href="css/cv.css">
</head>
<body>
    <nav><div><a href="index.html">Home</a><a class="active" href="cv.html">CV</a></div></nav>
    <section class="container">
        <div class="cv">
            <aside class="sidebar">
                <img src="images/profile.jpeg" alt="Profile Photo">
                <h2>Ndaru Satria Tama</h2>
                <p>Information Technology Student<br>Web Developer & UI/UX Designer</p>
                <div class="skill-list"><span>HTML</span><span>CSS</span><span>JavaScript</span></div>
            </aside>
            
            <main class="content">
                <section class="profile">
                    <h2>About Me</h2>
                    <p>I am an Information Technology student passionate about web development, UI/UX design, and creating modern digital experiences.</p>
                </section>
                
                <h2>Experience</h2>
                <div class="timeline-item">
                    <h3>2025 - Present</h3>
                    <h4>Web Developer | Personal Projects</h4>
                </div>
                
                <h2>Education</h2>
                <div class="education">
                    <h4>Information Technology</h4>
                    <p>Institut Teknologi Sepuluh Nopember (ITS)<br>2025 - Present</p>
                </div>
                
                <h2>My Skills</h2>
                <div class="skill-bars">
                    <div><label>HTML & CSS <b>90%</b></label><span><i style="width:90%"></i></span></div>
                </div>
            </main>
        </div>
    </section>
</body>
</html>
```
Kode CSS (`cv.css`):
```
body { margin: 0; background: #fdfaf6; color: #222; }
.container { padding: 70px 8%; }

.cv { 
    display: grid; 
    grid-template-columns: 310px 1fr; 
    background: white; 
    border-radius: 28px; 
    overflow: hidden; 
}
.sidebar { background: #101820; color: white; padding: 40px; }
.sidebar img { width: 140px; height: 140px; border-radius: 50%; object-fit: cover; }
.content { padding: 45px; }

.timeline-item { border-left: 3px solid #e07a5f; padding-left: 22px; margin-bottom: 28px; }
.skill-bars span { height: 10px; background: #ddd; border-radius: 10px; display: block; margin: 10px 0 18px; overflow: hidden; }
.skill-bars i { height: 100%; display: block; background: #e07a5f; border-radius: 10px; }

@media (max-width: 900px) {
    .cv { grid-template-columns: 1fr; }
}
```
Penjelasan Creative CV:

Halaman ini menampilkan riwayat hidup dengan pendekatan tata letak dua kolom (sidebar asimetris) menggunakan CSS Grid (`grid-template-columns: 310px 1fr`). Identitas visual dan foto ditempatkan di blok gelap sebelah kiri, sedangkan rincian profil, pengalaman kerja, pendidikan, dan metrik keahlian dijabarkan di area putih yang lebih luas di sebelah kanan.

### Requirements
#### Landing Page & Call to Action
Potongan Kode (`index.html`):
```
<div class="hero-buttons">
    <a class="btn" href="cv.html">View My CV</a>
</div>
```
Sebuah tautan jangkar (`<a>`) dirancang secara visual menyerupai tombol menggunakan kelas `.btn`. Atribut `href="cv.html"` berfungsi sebagai Call to Action yang langsung memindahkan pengunjung dari Landing Page menuju ke halaman Creative CV.

#### Kelengkapan Creative CV
Potongan Kode (`cv.html`):
```
<aside class="sidebar">
    <img src="images/profile.jpeg" alt="Profile Photo">
</aside>
<main class="content">
    <section class="profile"><h2>About Me</h2><p>I am an Information Technology student...</p></section>
    <div class="timeline-item"><h4>Web Developer | Personal Projects</h4></div>
    <div class="education"><h4>Information Technology</h4></div>
    <div class="skill-bars"><div><label>HTML & CSS</label><span><i style="width:90%"></i></span></div></div>
</main>
```
Seluruh elemen wajib CV telah disusun dalam tag semantik HTML. Foto profil berada di `.sidebar`, sedangkan deskripsi karakter (About Me), riwayat pengalaman (Experience), pendidikan (Education), dan bilah indikator kemampuan teknis (Skills) tertata secara berurutan di dalam `.content`.

#### Pseudo-Class
Potongan Kode (`index.css`):
```
.nav-links a::after { 
    width: 0; 
    transition: 0.3s;
}
.nav-links a:hover::after { 
    width: 100%; 
}
```
Interaktivitas dicapai menggunakan pseudo-class `:hover`. Ketika kursor menyorot menu navigasi, properti `width` pada elemen garis bawah berubah dari 0 menjadi 100%, menciptakan animasi pelebaran visual yang mulus.

#### Position
Potongan Kode (`index.css`):
```
nav { 
    position: sticky; 
    top: 0; 
}
.nav-links a::after { 
    position: absolute; 
    left: 0; 
    bottom: -8px; 
}
```
Properti `position: sticky;` menjamin batang navigasi akan mengunci posisinya di puncak jendela peramban (browser) meskipun pengguna menggulir halaman ke bawah. Properti `position: absolute;` digunakan untuk memposisikan garis dekorasi tepat di bawah teks menu tanpa mengganggu tata letak dokumen secara keseluruhan.

#### Display, Flex & Grid
Potongan Kode Display dan Flex (`index.css`) & Grid (`cv.css`):
```
.hero { 
    display: flex; 
    justify-content: space-between; 
}
```
```
.cv { 
    display: grid; 
    grid-template-columns: 310px 1fr; 
}
```
Flexbox (`display: flex;`) mengatur distribusi ruang horizontal antara bagian teks sambutan dan blok foto profil pada layar awal agar sejajar rapi. Sebaliknya, struktur CSS Grid (`display: grid;`) dikonfigurasi dengan `grid-template-columns: 310px 1fr;` untuk memotong area layar secara permanen menjadi panel kiri selebar 310px dan panel kanan yang bersifat meluas otomatis.

#### Responsive
Potongan Kode (`index.css` & `cv.css`):
```
@media (max-width: 800px) {
    .hero { 
        flex-direction: column; 
    }
}
```
```
@media (max-width: 900px) {
    .cv { 
        grid-template-columns: 1fr; 
    }
}
```
Menggunakan pendekatan blok `@media` (Media Queries) untuk mendeteksi ukuran layar pengguna. Saat lebar layar menyusut ke 800px atau 900px (ukuran Tablet dan Ponsel Pintar), orientasi baris Flexbox dikonversi menjadi kolom (`flex-direction: column`), dan sistem Grid ganda disederhanakan menjadi partisi tunggal (`grid-template-columns: 1fr`). Hal ini merespons keterbatasan ruang dengan menumpuk semua konten secara vertikal sehingga tidak ada elemen yang terpotong.
