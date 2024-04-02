<template>
  <div class="portfolio">
    <header class="header">
      <h1>My Portfolio</h1>
      <nav>
        <ul>
          <li><a href="#" class="nav-link">Home</a></li>
          <li><a href="#" class="nav-link">About</a></li>
          <li><a href="#" class="nav-link">Hobby</a></li>
          <li><a href="#" class="nav-link">Contact</a></li>
        </ul>
      </nav>
    </header>
    <main>
      <div class="gambar-bulat">
        <div class="gambar-mask">
          <img src="/public/20240402_140131.jpg" alt="Deskripsi gambar">
        </div>
      </div>
      <div class="intro">
        <h1>{{ title }}</h1>
        <div class="portfolio-content">
          <h2>Portofolio Saya</h2>
          <p>
            Saya adalah seorang mahasiswi bernama anggita wahyudini putri yang sedang menempuh pendidikan di Universitas Islam Riau, jurusan Teknik Informatika. Saya memiliki minat yang kuat dalam beberapa bidang, seperti pengembangan web, pemrograman, dan desain grafis. Selain itu, saya juga memiliki beberapa hobi, seperti membaca, menulis, dan memasak.
          </p>
          <h3>Hobi</h3>
          <ul>
            <li>Menulis</li>
            <li>Membaca buku</li>
            <li>Memasak</li>
          </ul>
          <h3>Pengalaman</h3>
          <ul>
            <li>Pernah bekerja di sebuah perusahaan</li>
          </ul>
          <p>
            Untuk menghubungi saya, silakan kunjungi halaman
            <router-link to="/contact">Kontak</router-link>.
          </p>
        </div>
      </div>
    </main>
    <footer>
      <p>&copy; 2024 Anggita wahyudini putri</p>
    </footer>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const title = ref('') // Define title as a ref
</script>

<style scoped>
.portfolio {
  display: flex;
  flex-direction: column;
  min-height: 100vh; /* Mengisi tinggi layar */
  background-color: #fff4e6; /* Nuansa cream */
}

.header {
  background-color: #ffcccc; /* Nuansa pink lebih gelap */
  padding: 10px 20px;
}

nav ul {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
}

nav ul li {
  margin-left: 10px;
}

.nav-link {
  color: white; /* Warna teks putih */
  text-decoration: none;
  padding: 5px 10px;
  border-radius: 5px;
  background-color: #4b7bec; /* Warna biru */
}

footer {
  background-color: #ffcccc; /* Nuansa pink lebih gelap */
  text-align: center;
  padding: 10px 0;
}

.intro {
  max-width: 600px;
  margin: 0 auto;
  text-align: center;
  background-color: #fff4e6; /* Nuansa cream */
  padding: 20px;
  border-radius: 5px;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
}

.gambar-bulat {
  width: 200px; /* Atur lebar gambar sesuai kebutuhan */
  height: 200px; /* Atur tinggi gambar sesuai kebutuhan */
  border-radius: 50%; /* Membuat sudut menjadi bulat */
  overflow: hidden; /* Memastikan gambar di dalam elemen yang bulat */
  margin: 0 auto; /* Memusatkan elemen gambar horizontal */
}

.gambar-mask {
  width: 100%;
  height: 100%;
  overflow: hidden;
  border-radius: 50%;
}

.gambar-mask img {
  width: 100%;
  height: auto;
  display: block;
}
</style>
