<script>
export default {
  name: 'NotFound',
}
</script>

<template>
  <div class="not-found">
    <div class="content">
      <h1 class="error-code">
        404
      </h1>
      <div class="divider" />
      <p class="error-message">
        抱歉,页面未找到
      </p>
      <router-link to="/" class="back-home">
        返回首页
      </router-link>
    </div>
  </div>
</template>

<style scoped>
.not-found {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100%;
  background: #fafafa;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
}

.content {
  text-align: center;
  padding: 3rem;
  max-width: 600px;
  width: 90%;
}

.error-code {
  font-size: 120px;
  font-weight: 200;
  color: #333;
  margin: 0;
  line-height: 1;
}

.divider {
  width: 60px;
  height: 2px;
  background: #333;
  margin: 2rem auto;
}

.error-message {
  font-size: 1.5rem;
  color: #666;
  margin: 1rem 0 2rem;
  font-weight: 300;
}

.back-home {
  display: inline-block;
  padding: 0.8rem 2rem;
  color: #333;
  border: 2px solid #333;
  border-radius: 2px;
  text-decoration: none;
  font-weight: 500;
  transition: all 0.3s ease;
}

.back-home:hover {
  background: #333;
  color: #fff;
}
</style>
