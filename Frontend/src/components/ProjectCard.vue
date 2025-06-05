<template>
  <a
    :href="project.repo"
    class="card"
    target="_blank"
    rel="noopener noreferrer"
    :title="`Ir al repositorio de ${project.name}`"
  >
    <h3>{{ project.name }}</h3>
    <p>Ver repositorio en GitHub</p>
    <svg
      xmlns="http://www.w3.org/2000/svg"
      class="icon"
      fill="none"
      viewBox="0 0 24 24"
      stroke="currentColor"
      stroke-width="2"
      aria-hidden="true"
    >
      <path
        stroke-linecap="round"
        stroke-linejoin="round"
        d="M14 5l7 7m0 0l-7 7m7-7H3"
      />
    </svg>
  </a>
</template>

<script setup>
defineProps({
  project: Object,
})
</script>

<style scoped>
.card {
  background: rgba(40, 56, 121, 0.6);
  border-radius: 15px;
  box-shadow: 0 0 10px #4b6af3aa;
  padding: 1.6rem 1.8rem;
  text-align: center;
  color: #c3d0ff;
  text-decoration: none;
  transition: all 0.25s ease;
  display: flex;
  flex-direction: column;
  justify-content: center;
  cursor: pointer;
  user-select: none;
  border: 1px solid transparent;
}

.card:hover {
  background: rgba(70, 90, 180, 0.9);
  box-shadow: 0 0 20px #7f9fffdd;
  border-color: #a1b9ff;
  color: #e1eaff;
  transform: translateY(-5px);
}

.card h3 {
  margin: 0 0 0.8rem;
  font-size: 1.3rem;
  font-weight: 700;
  text-shadow: 0 0 8px #5c7affaa;
}

.card p {
  margin: 0;
  font-size: 0.9rem;
  color: #a8b9ffcc;
}

.icon {
  margin-top: 0.9rem;
  width: 24px;
  height: 24px;
  stroke: #a0b5ffcc;
  align-self: center;
  transition: stroke 0.25s ease;
}

.card:hover .icon {
  stroke: #d0e1ff;
}
</style>
