<template>
  <div class="card">
    <div class="icon">
      {{ icon }}
    </div>

    <h2>{{ title }}</h2>

  <a
    :href="driveLink"
    target="_blank"
    rel="noopener noreferrer"
    class="btn"
  >
    Lihat Detail
    <span>→</span>
  </a>
  </div>
</template>

<script setup>
defineProps({
  icon: String,
  title: String,
  driveLink: String
})
</script>


<style scoped>
.card {
  min-height: 330px;
  background: white;
  border-radius: 16px;
  padding: 40px 28px;
  box-shadow: 0 8px 24px rgba(15, 23, 42, 0.08);
  border: 1px solid #e5e7eb;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.icon {
  width: 130px;
  height: 130px;
  border-radius: 50%;
  background: #fff0c2;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 54px;
  margin-bottom: 28px;
}

h2 {
  font-size: 22px;
  color: #071b45;
  margin-bottom: 45px;
  text-align: center;
}

.btn {
  background: #001a44;
  color: white;
  text-decoration: none;
  padding: 14px 34px;
  border-radius: 7px;
  font-size: 16px;
  display: inline-block;
  transition: all 0.3s ease;
}

.btn:hover {
  background: #002b70;
}

.btn span {
  color: #ffb703;
  margin-left: 10px;
}
</style>