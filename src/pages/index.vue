<script>
export default {
  name: 'Home',
  data() {
    return {
      projectIntro: {
        title: 'CSS 效果展示项目',
        description: '这是一个专注于展示各种CSS效果的项目库。在这里,您可以找到丰富多样的CSS动画和样式效果,帮助您在开发过程中快速实现所需的视觉效果。我们精心收集和整理了大量实用的CSS效果,并提供详细的代码示例和使用说明。',
      },
      cssEffects: [
        {
          id: 1,
          title: '页面布局',
          description: '上下固定，中间撑满的布局，使用flexbox',
          path: '/grid/flexbox',
          tags: ['布局'],
        },
      ],
    }
  },
}
</script>

<template>
  <div class="home">
    <section class="intro-section">
      <div class="intro-content">
        <h1 class="main-title">
          {{ projectIntro.title }}
          <span class="title-highlight">1.0</span>
        </h1>
        <p class="intro-text">
          {{ projectIntro.description }}
        </p>
        <div class="intro-features">
          <div class="feature">
            <span class="feature-number">100+</span>
            <span class="feature-text">CSS效果</span>
          </div>
          <div class="feature">
            <span class="feature-number">50+</span>
            <span class="feature-text">动画模板</span>
          </div>
          <div class="feature">
            <span class="feature-number">1000+</span>
            <span class="feature-text">代码示例</span>
          </div>
        </div>
      </div>
    </section>

    <section class="effects-section">
      <h2 class="section-title">
        效果展示
      </h2>
      <div class="effects-grid">
        <router-link v-for="effect in cssEffects" :key="effect.id" :to="effect.path" class="effect-card">
          <h3>{{ effect.title }}</h3>
          <p>{{ effect.description }}</p>
          <div class="tags">
            <span v-for="(tag, index) in effect.tags" :key="index" class="tag">
              {{ tag }}
            </span>
          </div>
          <span class="view-more">查看详情 →</span>
        </router-link>
      </div>
    </section>
  </div>
</template>

<style scoped>
.home {
  padding: 2rem;
  max-width: 1200px;
  margin: 0 auto;
}

.intro-section {
  text-align: center;
  margin-bottom: 4rem;
  padding: 4rem 2rem;
  background: linear-gradient(135deg, #f6f8ff 0%, #ffffff 100%);
  border-radius: 20px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
  position: relative;
  overflow: hidden;
}

.intro-section::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 6px;
  background: linear-gradient(90deg, #3182ce, #35c65c);
}

.intro-content {
  max-width: 900px;
  margin: 0 auto;
}

.main-title {
  font-size: 3.5rem;
  color: #1a1a1a;
  margin-bottom: 1.5rem;
  font-weight: 700;
  letter-spacing: -1px;
  line-height: 1.2;
}

.title-highlight {
  color: #3182ce;
  font-size: 2.5rem;
  vertical-align: super;
  margin-left: 0.5rem;
}

.intro-text {
  font-size: 1.25rem;
  color: #4a5568;
  line-height: 1.8;
  max-width: 800px;
  margin: 0 auto 3rem;
}

.intro-features {
  display: flex;
  justify-content: center;
  gap: 4rem;
  margin-top: 3rem;
}

.feature {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.feature-number {
  font-size: 2.5rem;
  font-weight: 700;
  color: #3182ce;
  margin-bottom: 0.5rem;
}

.feature-text {
  font-size: 1rem;
  color: #718096;
  font-weight: 500;
}

.section-title {
  text-align: center;
  font-size: 2rem;
  color: #2d3748;
  margin-bottom: 2.5rem;
}

.effects-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 1.5rem;
  padding: 0.5rem;
}

@media screen and (min-width: 640px) {
  .effects-grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 2rem;
  }
}

@media screen and (min-width: 1024px) {
  .effects-grid {
    grid-template-columns: repeat(3, 1fr);
    gap: 2.5rem;
  }
}

.effect-card {
  background: #fff;
  border-radius: 10px;
  padding: 1.5rem;
  box-shadow: 0 2px 12px rgba(0, 0, 0, 0.08);
  text-decoration: none;
  color: #333;
  transition: all 0.3s ease;
  border: 1px solid #edf2f7;
}

.effect-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.12);
}

.effect-card h3 {
  font-size: 1.25rem;
  color: #2d3748;
  margin-bottom: 1rem;
}

.effect-card p {
  color: #718096;
  margin-bottom: 1rem;
  font-size: 0.95rem;
  line-height: 1.6;
}

.tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin-bottom: 1rem;
}

.tag {
  background: #ebf4ff;
  color: #3182ce;
  padding: 0.25rem 0.75rem;
  border-radius: 15px;
  font-size: 0.8rem;
  font-weight: 500;
}

.view-more {
  display: inline-block;
  color: #3182ce;
  font-weight: 500;
  font-size: 0.9rem;
}
</style>
