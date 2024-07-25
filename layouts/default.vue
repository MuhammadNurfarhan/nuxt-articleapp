<template>
  <div>
    <div>
      <nav>
        <p>NuxtApp</p>
        <div class="nav-links">
          <NuxtLink to="/">Beranda</NuxtLink>
          <NuxtLink to="/about">Tentang</NuxtLink>
        </div>
      </nav>
      <slot />
    </div>
  </div>
</template>

<style scoped>
nav {
  padding: 20px;
  background-color: #a09c9c;
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 20px 0;
}

nav p {
  font-size: 24px;
  color: #edf0f3;
  font-weight: bold;
  letter-spacing: 1px;
  text-transform: uppercase;
  text-shadow: 1px 1px 2px #000;
  text-decoration: none;
  line-height: 1.2;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

.nav-links {
  display: flex;
  gap: 20px;
  justify-content: flex-end;
  flex: 1;
}

a {
  text-decoration: none;
  color: #edf0f3;
  font-size: 20px;
}

a:hover {
  text-decoration: underline;
}
</style>
