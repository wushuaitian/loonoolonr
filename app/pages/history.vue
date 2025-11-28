<!-- app/pages/history.vue -->
<template>
  <div class="history-page">
    <!-- 顶部导航 -->
    <header class="navbar">
      <div class="navbar-inner">
        <!-- 左侧 Logo -->
        <div class="nav-left">
          <img src="/imag/logo.png" alt="Loonool Logo" class="logo-img" />
          <span class="logo-text">Loonool</span>
        </div>

        <!-- 中间导航 -->
        <nav class="nav-center">
          <NuxtLink to="/" class="nav-link">首页</NuxtLink>
          <NuxtLink to="/detect" class="nav-link">检测查重</NuxtLink>
          <NuxtLink to="/history" class="nav-link">历史结果</NuxtLink>
          <NuxtLink to="/help" class="nav-link">了解更多</NuxtLink>

          <button class="nav-link nav-lang" type="button">
            选择语言
            <span class="lang-caret"></span>
          </button>
        </nav>

        <!-- 右侧按钮 -->
        <div class="nav-right">
          <button type="button" class="btn-outline">登陆</button>
          <button type="button" class="btn-solid">注册</button>
        </div>
      </div>
    </header>

    <!-- Hero 主区域 -->
    <main class="hero">
      <div class="hero-inner">
        <h1 class="hero-title">
          视觉内容进入商业<br />
          世界前的安全层。
        </h1>

        <p class="hero-subtitle">
          查重 · 存证 · 维权 —— 一站式原创设计保护平台
        </p >

        <!-- 上传区域 -->
        <div class="upload-row">
          <!-- 左侧小图标 + hover 文案 -->
          <div class="hover-left">
            <div class="hover-icon-wrap">
              <img src="/imag/icon-image.png" alt="image icon" />
            </div>
            <span class="hover-text">👆 hover</span>
          </div>

          <!-- 中间上传条 -->
          <div class="upload-bar">
            <div class="upload-image-icon">
              <img src="/imag/icon-image.png" alt="image icon" />
            </div>

            <div class="upload-text-line">
              <span class="upload-text-muted">点击添加图片</span>
              <span class="upload-text-link">点击添加图片</span>
              <span class="upload-hover-badge">👈 hover</span>
            </div>

            <button class="btn-send" type="button">
              <img
                src="/imag/icon-send.png"
                alt="send"
                class="send-img"
              />
            </button>
          </div>
        </div>

        <p class="upload-tip">
          上传最大 5MB 的 JPEG\PNG 或 GIF 格式图片，即可立即进行原创性验证。
        </p >
      </div>
    </main>
  </div>
</template>

<script setup>
// 本页为静态展示，无逻辑
</script>

<style>
/* 整体背景：白 + 底部彩色模糊背景图 */
.history-page {
   background:
    radial-gradient(circle at 70% 80%, #d4e9ff 0%, transparent 45%),
    radial-gradient(circle at 30% 85%, #ffddee 0%, transparent 50%),
    radial-gradient(circle at 50% 95%, #e9ddff 0%, transparent 55%),
    #ffffff;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  font-family: -apple-system, BlinkMacSystemFont, 'SF Pro Text', system-ui,
    sans-serif;
}

/* 顶部导航 */
.navbar {
  width: 100%;
  height: 72px;
  background: #ffffff;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0 32px;
  box-shadow: 0 1px 4px rgba(15, 23, 42, 0.04);
}

.navbar-inner {
  width: 100%;
  max-width: 1280px;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

/* 左侧 Logo */
.nav-left {
  display: flex;
  align-items: center;
  gap: 8px;
}

.logo-img {
  width: 26px;
  height: 26px;
  border-radius: 8px;
  object-fit: contain;
}

.logo-text {
  font-size: 18px;
  font-weight: 600;
  color: #2563eb;
  letter-spacing: 0.3px;
}

/* 中间导航 */
.nav-center {
  display: flex;
  align-items: center;
  gap: 28px;
}

.nav-link {
  border: none;
  background: transparent;
  padding: 4px 0;
  font-size: 14px;
  color: #6b7280;
  cursor: pointer;
  text-decoration: none;
  position: relative;
}

.nav-link:hover {
  color: #111827;
}

.nav-link.router-link-exact-active {
  color: #2563eb;
  font-weight: 600;
}

.nav-link.router-link-exact-active::after {
  content: "";
  position: absolute;
  left: 0;
  right: 0;
  bottom: -8px;
  height: 2px;
  border-radius: 999px;
  background: #2563eb;
}

/* 选择语言下拉箭头 */
.nav-lang {
  display: inline-flex;
  align-items: center;
  gap: 4px;
}

.lang-caret {
  width: 0;
  height: 0;
  border-left: 4px solid transparent;
  border-right: 4px solid transparent;
  border-top: 5px solid #9ca3af;
}

/* 右侧按钮 */
.nav-right {
  display: flex;
  align-items: center;
  gap: 12px;
}

.btn-outline,
.btn-solid {
  padding: 8px 26px;
  border-radius: 999px;
  font-size: 14px;
  cursor: pointer;
  border: 1px solid transparent;
  transition: all 0.15s ease-out;
}

.btn-outline {
  border-color: #2563eb;
  color: #2563eb;
  background: #ffffff;
}

.btn-outline:hover {
  background: #eff6ff;
}

.btn-solid {
  background: #2563eb;
  color: #ffffff;
  border-color: #2563eb;
  box-shadow: 0 8px 18px rgba(37, 99, 235, 0.35);
}

.btn-solid:hover {
  background: #1d4ed8;
}

/* Hero 主区域 */
.hero {
  display: flex;
  justify-content: center;
}

.hero-inner {
  max-width: 1040px;
  width: 100%;
  text-align: center;
  padding: 120px 16px 140px;
  margin: 0 auto;
}

.hero-title {
  font-size: 64px;
  font-weight: 700;
  line-height: 1.18;
  color: #111827;
  margin: 0 0 32px;
}

.hero-subtitle {
  font-size: 14px;
  letter-spacing: 0.18em;
  color: #6b7280;
  margin-bottom: 56px;
  font-weight: 700;
}

/* 上传区域：左侧小图标 + 中间条 */
.upload-row {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 32px;
  margin-bottom: 18px;
}

/* 左侧 hover 图标 */
.hover-left {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 6px;
  font-size: 11px;
}

.hover-icon-wrap {
  width: 32px;
  height: 32px;
  border-radius: 12px;
  background: rgba(255, 255, 255, 0.85);
  box-shadow: 0 10px 24px rgba(15, 23, 42, 0.18);
  display: flex;
  align-items: center;
  justify-content: center;
}

.hover-icon-wrap img {
  width: 20px;
  height: 20px;
  display: block;
}

.hover-text {
  color: #111827;
}

/* 中间上传条 */
.upload-bar {
  width: 803px;            /* 固定宽度 803px */
  max-width: 100%;
  height: 78px;            /* 固定高度 78px */
  border-radius: 39px;     /* 圆角 39px */
  background: #ffffff;
  padding: 0 24px 0 28px;
  box-shadow:
    0 22px 48px rgba(15, 23, 42, 0.16),
    0 0 0 1px rgba(209, 213, 219, 0.5);
  display: flex;
  align-items: center;
}

/* 条内左侧图标 */
.upload-image-icon {
  flex-shrink: 0;
  margin-right: 16px;
}

.upload-image-icon img {
  width: 30px;
  height: 30px;
  display: block;
}

/* 条内文字 */
.upload-text-line {
  display: flex;
  align-items: center;
  gap: 14px;
  font-size: 13px;
  flex: 1;
}

.upload-text-muted {
  color: #b5bcc8;
}

.upload-text-link {
  color: #2563eb;
}

.upload-hover-badge {
  font-size: 12px;
  color: #facc15; /* 黄色 hover 文案效果 */
}

/* 右侧纸飞机按钮 */
.btn-send {
  border: none;
  background: transparent;
  padding: 0;
  cursor: pointer;
}

.send-img {
  width: 44px;
  height: 44px;
  display: block;
}

/* 底部说明文字 */
.upload-tip {
  margin-top: 10px;
  font-size: 12px;
  color: #a78bfa; /* 接近截图里偏紫的说明文字 */
}
</style>