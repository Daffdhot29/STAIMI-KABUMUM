<template>
  <div class="page">
    <!-- Sidebar -->
    <aside class="sidebar">
      <img src="./assets/logo.png" alt="Logo Madinatul Ilmi" class="logo" />

      <nav class="menu">
        <a class="menu-item active" href="#">
          <span>⌂</span>
          Bagian Umum
        </a>

        <a class="menu-item" href="#">
          <span>▣</span>
          Keuangan
        </a>

        <a class="menu-item" href="#">
          <span>▥</span>
          Sarana dan Prasarana
        </a>

        <a class="menu-item" href="#">
          <span>👥</span>
          Kepegawaian
        </a>
      </nav>

      <div class="sidebar-footer">
        <div class="footer-icon">👥</div>
        <p>Divisi Bagian Administrasi,<br />Umum dan Kepegawaian</p>
      </div>
    </aside>

    <!-- Main Content -->
    <main class="main">
      <header class="topbar">
        <button class="hamburger">☰</button>

      
      </header>

      <section class="hero">
        <div class="hero-text">
          <h1>BAGIAN UMUM</h1>
          <div class="line"></div>

          <h3>
            Divisi Bagian Administrasi,<br />
            Umum dan Kepegawaian.
          </h3>

          <p>
            Bertanggung jawab dalam pengelolaan administrasi umum,
            layanan internal, pengelolaan aset, sarana dan prasarana,
            serta dukungan operasional untuk menunjang kegiatan institusi
            secara efektif dan efisien.
          </p>
        </div>

        <img src="./assets/gedung.jpeg" alt="Gedung Kampus" class="hero-img" />
      </section>

      <section class="cards">
        <ServiceCard
          icon="💼"
          title="KEUANGAN"
        />

        <ServiceCard
          icon="🏢"
          title="SARANA DAN PRASARANA"
        />

        <ServiceCard
          icon="👥"
          title="KEPEGAWAIAN"
        />
      </section>

      <footer>
        © 2026 STAI Madinatul Ilmi
      </footer>
    </main>
  </div>
</template>

<script setup>
import ServiceCard from './components/ServiceCard.vue'
</script>

<style scoped>
.page {
  min-height: 100vh;
  display: flex;
  background: #f8fafc;
  font-family: Arial, sans-serif;
  color: #071b45;
}

.sidebar {
  width: 300px;
  background: linear-gradient(180deg, #001a44, #00102d);
  color: white;
  padding: 32px 24px;
  display: flex;
  flex-direction: column;
}

.logo {
  width: 230px;
  margin-bottom: 60px;
}

.menu {
  display: flex;
  flex-direction: column;
  gap: 24px;
}

.menu-item {
  color: white;
  text-decoration: none;
  font-size: 18px;
  padding: 16px 18px;
  border-radius: 10px;
  display: flex;
  align-items: center;
  gap: 16px;
}

.menu-item.active {
  background: rgba(255, 255, 255, 0.1);
  color: #ffb703;
  border-left: 5px solid #ffb703;
}

.sidebar-footer {
  margin-top: auto;
  border-top: 1px solid rgba(255, 255, 255, 0.2);
  padding-top: 28px;
  display: flex;
  gap: 14px;
  align-items: center;
}

.footer-icon {
  background: white;
  color: #001a44;
  padding: 10px;
  border-radius: 8px;
}

.sidebar-footer p {
  font-size: 15px;
  line-height: 1.5;
}

.main {
  flex: 1;
}

.topbar {
  height: 90px;
  background: white;
  box-shadow: 0 2px 12px rgba(0, 0, 0, 0.06);
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 36px;
}

.hamburger {
  background: none;
  border: none;
  font-size: 28px;
  cursor: pointer;
}

.admin {
  display: flex;
  align-items: center;
  gap: 16px;
  font-size: 18px;
}

.avatar {
  width: 42px;
  height: 42px;
  background: #d9dee8;
  border-radius: 50%;
}

.hero {
  padding: 48px 44px 32px;
  display: grid;
  grid-template-columns: 1fr 1.5fr;
  gap: 48px;
  align-items: center;
}

.hero-text h1 {
  font-size: 46px;
  font-weight: 900;
  color: #0B1F52;
  letter-spacing: -1px;
}

.line {
  width: 64px;
  height: 5px;
  background: #ffb703;
  border-radius: 10px;
  margin: 24px 0;
}

.hero-text h3 {
  font-size: 23px;
  line-height: 1.5;
  margin-bottom: 26px;
  font-weight: 500;
}

.hero-text p {
  font-size: 15px;
  line-height: 1.7;
  color: #1f2937;
}

.hero-img {
  width: 100%;
  height: 360px;
  object-fit: cover;
  border-radius: 18px;
}

.cards {
  padding: 0 44px 36px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 28px;
}

footer {
  text-align: center;
  padding: 18px;
  color: #344767;
  font-size: 14px;
}

/* Responsive */
@media (max-width: 900px) {
  .page {
    flex-direction: column;
  }

  .sidebar {
    width: auto;
  }

  .hero {
    grid-template-columns: 1fr;
  }

  .cards {
    grid-template-columns: 1fr;
  }
}
</style>