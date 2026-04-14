[qscm.html](https://github.com/user-attachments/files/26694859/qscm.html)
<!DOCTYPE html>
<html lang="zh-TW">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>TikTok旅行推廣招募 - 全晟傳媒</title>
<!-- 引入外部依赖（增加备用CDN） -->
<script src="https://cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js" onerror="console.log('particles.js加载失败，使用备用方案')"></script>
<script src="https://cdn.jsdelivr.net/npm/countup.js@2.8.0/dist/countUp.umd.min.js" onerror="console.log('countUp.js加载失败，使用静态数字')"></script>
<!-- 引入Font Awesome增强图标质感 -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<style>
/* 全局重置与基础样式 - 提升高级感 */
*{margin:0;padding:0;box-sizing:border-box;font-family:'Inter', -apple-system, BlinkMacSystemFont, "PingFang SC", "Microsoft YaHei", sans-serif}
:root {
  --primary: #7a94ff;
  --primary-dark: #4a6cff;
  --primary-light: #9ab0ff;
  --bg-dark: #0a1028;
  --bg-card: #121a33;
  --bg-card-hover: #1a244a;
  --text-primary: #e6edff;
  --text-secondary: #c8d4ff;
  --text-tertiary: #b0c4ff;
  --border-light: rgba(90,110,220,0.15);
  --shadow-sm: 0 4px 12px rgba(0,0,0,0.1);
  --shadow-md: 0 8px 24px rgba(0,0,0,0.2);
  --shadow-lg: 0 15px 35px rgba(90,110,220,0.15);
  --shadow-glow: 0 0 30px rgba(90, 110, 220, 0.45), 0 0 60px rgba(122, 148, 255, 0.2);
  --transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}

/* 平滑滚动 */
html {
  scroll-behavior: smooth;
}

#particles-js{position:fixed;top:0;left:0;width:100%;height:100%;z-index:-1;background:var(--bg-dark);}
body{background:var(--bg-dark);color:var(--text-primary);line-height:1.7;position:relative;}
.container{max-width:1200px;margin:0 auto;padding:0 25px;position:relative;z-index:1;}

/* 导航栏 - 新增高级导航 */
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background: rgba(10,16,40,0.8);
  backdrop-filter: blur(15px);
  z-index: 9998;
  border-bottom: 1px solid var(--border-light);
  transition: var(--transition);
}
.navbar-scrolled {
  background: rgba(10,16,40,0.95);
  box-shadow: var(--shadow-sm);
}
.navbar-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 25px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 70px;
}
.logo {
  font-size: 22px;
  font-weight: 700;
  color: var(--primary);
  text-decoration: none;
  display: flex;
  align-items: center;
  gap: 8px;
}
.logo i {
  font-size: 24px;
}
.nav-links {
  display: flex;
  gap: 30px;
}
.nav-link {
  color: var(--text-secondary);
  text-decoration: none;
  font-size: 16px;
  font-weight: 500;
  position: relative;
  transition: var(--transition);
}
.nav-link:hover {
  color: var(--primary);
}
.nav-link::after {
  content: "";
  position: absolute;
  bottom: -4px;
  left: 0;
  width: 0;
  height: 2px;
  background: linear-gradient(90deg, var(--primary-dark), var(--primary));
  transition: var(--transition);
}
.nav-link:hover::after {
  width: 100%;
}
.mobile-menu-btn {
  display: none;
  font-size: 24px;
  color: var(--primary);
  cursor: pointer;
}

/* 封面样式 - 升级高级光效和层次感 */
.cover{
  background:linear-gradient(135deg, rgba(10,15,40,0.85),rgba(20,30,70,0.95)),url('https://picsum.photos/id/1036/1920/1080') center/cover no-repeat;
  color:#fff;text-align:center;padding:200px 30px 160px;border-radius:0;margin:70px 0 60px;
  box-shadow:0 0 60px rgba(90,110,220,0.4);position:relative;overflow:hidden;
  border-bottom: 1px solid var(--border-light);
}
/* 封面高级流动光效 */
.cover::after {
  content: "";
  position: absolute;
  top: 0;
  left: -100%;
  width: 200%;
  height: 100%;
  background: linear-gradient(90deg, 
    transparent, 
    rgba(122, 148, 255, 0.15), 
    transparent);
  animation: light-flow 6s infinite linear;
}
@keyframes light-flow {
  0% { left: -100%; }
  100% { left: 100%; }
}
/* 封面粒子点缀 */
.cover::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: radial-gradient(circle at 30% 20%, rgba(122,148,255,0.1) 0%, transparent 40%),
              radial-gradient(circle at 70% 80%, rgba(74,108,255,0.1) 0%, transparent 40%);
  z-index: 1;
}
.cover-content {
  position: relative;
  z-index: 2;
}
.cover h1{
  font-size: clamp(3rem, 6vw, 4.5rem);
  margin-bottom: 25px;
  font-weight: 800;
  text-shadow:0 0 30px rgba(90,110,220,0.5);
  background: linear-gradient(90deg, var(--primary-light), #ffffff, var(--primary));
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  letter-spacing: 1.5px;
  line-height: 1.2;
}
.cover p{
  font-size: clamp(1.2rem, 3vw, 1.8rem);
  opacity: 0.95;
  margin-bottom: 30px;
  max-width: 800px;
  margin-left: auto;
  margin-right: auto;
}
.cover-tag{
  display:inline-block;
  background:rgba(122,148,255,0.15);
  padding:10px 24px;
  border-radius: 50px;
  font-size: 16px;
  margin: 0 10px 10px;
  backdrop-filter: blur(10px);
  border: 1px solid rgba(122,148,255,0.2);
  transition: var(--transition);
}
.cover-tag:hover {
  background:rgba(122,148,255,0.25);
  transform: translateY(-2px);
}

/* 页面板块样式 - 极致高级感 */
.page{
  background: linear-gradient(135deg, 
    var(--bg-card) 0%, 
    var(--bg-card-hover) 50%, 
    #202c58 100%);
  border-radius: 24px;
  margin: 40px 0;
  padding: 60px 40px;
  box-shadow: var(--shadow-md);
  transition: var(--transition);
  border: 1px solid var(--border-light);
  backdrop-filter: blur(15px);
  position: relative;
  overflow: hidden;
}
/* 板块高级光效点缀 */
.page::before {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  width: 300px;
  height: 300px;
  background: radial-gradient(circle, rgba(122,148,255,0.05) 0%, transparent 70%);
  border-radius: 50%;
  transform: translate(50%, -50%);
  z-index: 0;
}
.page:hover{
  transform: translateY(-8px);
  box-shadow: var(--shadow-lg);
  border-color: rgba(90,110,220,0.25);
}
.page-content {
  position: relative;
  z-index: 1;
}
.title{
  font-size: clamp(1.8rem, 4vw, 2.5rem);
  color:var(--primary);
  text-align:center;
  margin-bottom: 40px;
  font-weight: 700;
  position:relative;
  text-shadow:0 0 20px rgba(122,148,255,0.6);
  letter-spacing: 1px;
}
.title::after{
  content:"";
  width: 100px;
  height: 6px;
  background:linear-gradient(90deg,var(--primary-dark),var(--primary));
  border-radius: 5px;
  display:block;
  margin:15px auto 0;
  box-shadow:0 0 15px rgba(90,110,220,0.5);
}

/* 核心数据样式 - 增强高级光效 */
.stats-box{
  display:flex;
  flex-wrap:wrap;
  gap: 35px;
  justify-content:center;
  margin: 50px 0;
}
.stats-item{
  text-align:center;
  padding: 30px 25px;
  width: 240px;
  background:rgba(20,30,70,0.4);
  border-radius: 20px;
  border:1px solid rgba(90,110,220,0.25);
  transition:var(--transition);
  position:relative;
  overflow:hidden;
  backdrop-filter: blur(10px);
}
.stats-item::before{
  content:"";
  position:absolute;
  top:0;
  left:0;
  width:100%;
  height:5px;
  background:linear-gradient(90deg,var(--primary-dark),var(--primary));
}
/* 数据卡片悬停光效 */
.stats-item::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(135deg, rgba(122,148,255,0.05) 0%, transparent 70%);
  opacity: 0;
  transition: var(--transition);
}
.stats-item:hover{
  transform:scale(1.08);
  box-shadow:0 10px 20px rgba(90,110,220,0.25);
  background:rgba(20,30,70,0.5);
}
.stats-item:hover::after {
  opacity: 1;
}
.stats-num{
  font-size: clamp(2rem, 5vw, 3rem);
  font-weight: 800;
  color:var(--primary);
  margin-bottom: 10px;
  text-shadow: 0 0 20px rgba(122, 148, 255, 0.9),
               0 0 40px rgba(122, 148, 255, 0.6);
  position: relative;
  z-index: 1;
}
.stats-text{
  font-size: 18px;
  color:var(--text-secondary);
  line-height: 1.4;
  position: relative;
  z-index: 1;
}

/* 图片容器样式 - 高级加载和过渡 */
.img-box{
  width:100%;
  height: auto;
  min-height: 400px;
  border-radius: 20px;
  overflow:hidden;
  margin: 25px 0;
  border:1px solid rgba(90,110,220,0.25);
  background: linear-gradient(rgba(20,30,70,0.6), rgba(30,40,90,0.6));
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--primary);
  font-size: 18px;
  position: relative;
}

/* TikTok核心优势图片网格 - 新增样式 */
.tiktok-advantage-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 30px;
  margin: 40px 0;
}
.tiktok-advantage-item {
  border-radius: 16px;
  overflow: hidden;
  border: 1px solid rgba(90,110,220,0.25);
  transition: var(--transition);
  box-shadow: var(--shadow-sm);
}
.tiktok-advantage-item:hover {
  transform: translateY(-8px);
  box-shadow: var(--shadow-md);
  border-color: rgba(122,148,255,0.4);
}
.tiktok-advantage-item img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
  transition: var(--transition);
}
.tiktok-advantage-item:hover img {
  transform: scale(1.03);
  filter: brightness(1.05);
}

/* 图片加载骨架屏 */
.img-box::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(122,148,255,0.1), transparent);
  animation: skeleton-loading 1.5s infinite;
  opacity: 0;
  z-index: 1;
}
.img-box img:not(.loaded) + .img-box::before {
  opacity: 1;
}
@keyframes skeleton-loading {
  0% { transform: translateX(-100%); }
  100% { transform: translateX(100%); }
}
.img-box img, .multi-img-item img, .gallery-item img {
  width:100%;
  height:100%;
  object-fit:cover;
  transition: all 0.6s cubic-bezier(0.4, 0, 0.2, 1);
  opacity: 1;
}
.img-box img:hover{
  transform:scale(1.15);
  filter:brightness(1.15) contrast(1.05);
}

/* 多图展示容器 - 高级布局 */
.multi-img-box{
  display:flex;
  gap: 20px;
  margin: 40px 0;
  flex-wrap:wrap;
}
.multi-img-item{
  flex:1;
  min-width: 300px;
  height: 200px;
  border-radius: 16px;
  overflow:hidden;
  border:1px solid rgba(90,110,220,0.25);
  position: relative;
}
/* 多图高级遮罩 */
.multi-img-item::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(to bottom, transparent 0%, rgba(10,16,40,0.4) 100%);
  transition: var(--transition);
}
.multi-img-item:hover::after {
  background: linear-gradient(to bottom, transparent 0%, rgba(10,16,40,0.2) 100%);
}
.multi-img-item img:hover{
  transform:scale(1.1);
  filter:brightness(1.1) contrast(1.05);
}

/* 图片画廊样式 - 高级网格 */
.gallery-box {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 20px;
  margin: 40px 0;
}
.gallery-item {
  height: 220px;
  border-radius: 16px;
  overflow: hidden;
  border: 1px solid rgba(90,110,220,0.25);
  position: relative;
  cursor: pointer;
  transition: var(--transition);
}
.gallery-item::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(10,15,40,0.3);
  transition: var(--transition);
}
.gallery-item:hover {
  transform: translateY(-5px);
  box-shadow: var(--shadow-md);
}
.gallery-item:hover::after {
  background: rgba(10,15,40,0);
}
.gallery-item img:hover {
  transform: scale(1.15);
  filter: brightness(1.2) contrast(1.05);
}

/* 轮播图样式 - 高级交互 */
.slider-box {
  width: 100%;
  height: 450px;
  border-radius: 20px;
  overflow: hidden;
  margin: 40px 0;
  position: relative;
  border: 1px solid rgba(90,110,220,0.25);
  box-shadow: var(--shadow-md);
}
.slider-container {
  display: flex;
  width: 100%;
  height: 100%;
  transition: transform 0.7s cubic-bezier(0.4, 0, 0.2, 1);
}
.slider-item {
  min-width: 100%;
  height: 100%;
  position: relative;
}
.slider-item::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(to bottom, rgba(10,16,40,0.2) 0%, rgba(10,16,40,0.6) 100%);
}
.slider-item img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.slider-nav {
  position: absolute;
  bottom: 30px;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  gap: 12px;
  z-index: 2;
}
.slider-dot {
  width: 14px;
  height: 14px;
  border-radius: 50%;
  background: rgba(255,255,255,0.4);
  cursor: pointer;
  transition: var(--transition);
  border: 2px solid transparent;
}
.slider-dot.active {
  background: var(--primary);
  transform: scale(1.3);
  box-shadow: 0 0 15px rgba(122,148,255,0.9);
  border-color: rgba(255,255,255,0.5);
}
.slider-arrow {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background: rgba(10,15,40,0.8);
  color: var(--primary);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 24px;
  cursor: pointer;
  transition: var(--transition);
  z-index: 10;
  border: 1px solid rgba(122,148,255,0.3);
}
.slider-arrow:hover {
  background: var(--primary);
  color: white;
  box-shadow: 0 0 20px rgba(122,148,255,0.9);
  transform: translateY(-50%) scale(1.1);
}
.slider-prev {
  left: 25px;
}
.slider-next {
  right: 25px;
}

/* 优势板块样式 - 增强高级交互 */
.advantage-box{
  display:flex;
  flex-wrap:wrap;
  gap: 30px;
  margin-top: 30px;
}
.advantage-item{
  flex:1;
  min-width: 320px;
  background:rgba(20,30,70,0.5);
  padding: 35px 30px;
  border-radius: 20px;
  border-left: 6px solid var(--primary-dark);
  box-shadow: var(--shadow-sm);
  border:1px solid rgba(90,110,220,0.15);
  transition:var(--transition);
  backdrop-filter: blur(10px);
  position: relative;
  overflow: hidden;
}
/* 优势卡片光效 */
.advantage-item::after {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  width: 100px;
  height: 100px;
  background: radial-gradient(circle, rgba(122,148,255,0.1) 0%, transparent 70%);
  border-radius: 50%;
  transform: translate(50%, -50%);
  transition: var(--transition);
}
.advantage-item:hover{
  transform:translateX(8px);
  box-shadow:0 10px 25px rgba(90,110,220,0.2);
  background:rgba(20,30,70,0.6);
  border-left-color: var(--primary);
}
.advantage-item:hover::after {
  transform: translate(40%, -40%) scale(1.2);
}
.advantage-item h3{
  color:var(--primary);
  margin-bottom: 15px;
  font-size: 24px;
  display:flex;
  align-items:center;
  gap: 10px;
  letter-spacing: 0.5px;
}
.advantage-item h3::before{
  content:"✨";
  font-size: 20px;
}
.advantage-item p{
  margin: 10px 0;
  color:var(--text-tertiary);
  font-size: 16px;
  line-height: 1.8;
}

/* 公司介绍样式 - 高级排版 */
.company-desc{
  font-size: 18px;
  line-height: 2.2;
  color:var(--text-primary);
  text-align:center;
  margin: 25px 0;
  letter-spacing: 0.3px;
  max-width: 900px;
  margin-left: auto;
  margin-right: auto;
}
.company-desc p{
  margin: 20px 0;
  padding: 0 20px;
}

/* 合作公司样式 - 高级卡片 */
.partner-box{
  display:flex;
  flex-wrap:wrap;
  gap: 30px;
  justify-content:center;
  margin: 40px 0;
}
.partner-item{
  width: 240px;
  height: 90px;
  background:rgba(255,255,255,0.08);
  border-radius: 16px;
  display:flex;
  align-items:center;
  justify-content:center;
  transition:var(--transition);
  border:1px solid rgba(90,110,220,0.2);
  backdrop-filter: blur(10px);
  position: relative;
  overflow: hidden;
}
/* 合作伙伴卡片光效 */
.partner-item::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(135deg, rgba(122,148,255,0.05) 0%, transparent 70%);
  opacity: 0;
  transition: var(--transition);
}
.partner-item:hover{
  transform:scale(1.1);
  background:rgba(255,255,255,0.12);
  box-shadow:0 0 20px rgba(122,148,255,0.4);
  border-color: rgba(122,148,255,0.3);
}
.partner-item:hover::before {
  opacity: 1;
}
.partner-name{
  font-size: 18px;
  color:var(--primary);
  font-weight: 600;
  text-align:center;
  line-height: 1.5;
  position: relative;
  z-index: 1;
}

/* 团队板块样式 - 高级卡片 */
.team-box{
  display:flex;
  flex-wrap:wrap;
  gap: 40px;
  justify-content:center;
  margin-top: 40px;
}
.team-item{
  width: 340px;
  text-align:center;
  padding: 35px 30px;
  background:rgba(20,30,70,0.3);
  border-radius: 20px;
  border:1px solid rgba(90,110,220,0.15);
  transition:var(--transition);
  backdrop-filter: blur(10px);
  position: relative;
  overflow: hidden;
}
/* 团队卡片高级光效 */
.team-item::before {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(to top, rgba(122,148,255,0.05) 0%, transparent 70%);
  transition: var(--transition);
}
.team-item:hover{
  transform:translateY(-10px);
  box-shadow:0 15px 30px rgba(90,110,220,0.2);
  background:rgba(20,30,70,0.4);
  border-color: rgba(90,110,220,0.25);
}
.team-avatar{
  width: 130px;
  height: 130px;
  border-radius: 50%;
  background:linear-gradient(135deg,var(--primary-dark),var(--primary));
  margin:0 auto 25px;
  display:flex;
  align-items:center;
  justify-content:center;
  color:#fff;
  font-size: 52px;
  box-shadow:0 0 25px rgba(90,110,220,0.4);
  position: relative;
  z-index: 1;
}
.team-item h3{
  font-size: 26px;
  color:#fff;
  margin-bottom: 15px;
  position: relative;
  z-index: 1;
}
.team-item p{
  color:var(--text-tertiary);
  margin: 8px 0;
  font-size: 16px;
  position: relative;
  z-index: 1;
}

/* 按钮样式 - 极致高级光效 */
.btn{
  display:inline-block;
  background: linear-gradient(135deg, 
    var(--primary-dark) 0%, 
    var(--primary) 50%, 
    var(--primary-light) 100%);
  color:#fff;
  padding: 20px 50px;
  border-radius: 50px;
  text-decoration:none;
  font-weight: 700;
  font-size: 18px;
  margin-top: 30px;
  box-shadow:0 0 25px rgba(90,110,220,0.4);
  transition:var(--transition);
  border:1px solid rgba(255,255,255,0.15);
  position: relative;
  overflow: hidden;
}
/* 按钮高级光效 */
.btn::before {
  content: "";
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
  transition: var(--transition);
}
.btn:hover{
  transform:scale(1.08);
  box-shadow: var(--shadow-glow);
  border-color: rgba(255,255,255,0.25);
}
.btn:hover::before {
  left: 100%;
}

/* 悬浮按钮 - 升级 */
.float-btn{
  position:fixed;
  right: 40px;
  bottom: 40px;
  background:linear-gradient(135deg,var(--primary-dark),var(--primary));
  width: 70px;
  height: 70px;
  border-radius: 50%;
  display:flex;
  align-items:center;
  justify-content:center;
  font-size: 28px;
  color:#fff;
  box-shadow:0 0 25px rgba(90,110,220,0.6);
  z-index:9999;
  cursor:pointer;
  transition:var(--transition);
  border: 1px solid rgba(255,255,255,0.2);
}
.float-btn:hover{
  transform:scale(1.15) rotate(5deg);
  box-shadow:0 0 40px rgba(90,110,220,0.8);
}

/* 通用文本样式 - 高级排版 */
.desc{
  text-align:center;
  line-height: 2.2;
  font-size: 18px;
  color:var(--text-secondary);
  max-width: 900px;
  margin-left: auto;
  margin-right: auto;
}
.benefit-desc{
  text-align:left;
  font-size: 20px;
  line-height: 2.8;
  margin: 25px 0;
  color:var(--text-primary);
  max-width: 1000px;
  margin-left: auto;
  margin-right: auto;
}
.benefit-desc p{
  margin: 15px 0;
  padding-left: 20px;
  border-left: 4px solid var(--primary);
  position: relative;
}
/* 优势文本装饰 */
.benefit-desc p::before {
  content: "";
  position: absolute;
  left: -20px;
  top: 50%;
  width: 8px;
  height: 8px;
  background: var(--primary);
  border-radius: 50%;
  transform: translateY(-50%);
}

/* 鼠标光效 - 升级 */
.cursor-light{
  position:absolute;
  width: 25px;
  height: 25px;
  border-radius: 50%;
  background:rgba(122,148,255,0.2);
  border:2px solid rgba(122,148,255,0.6);
  pointer-events:none;
  z-index:9999;
  transition:all 0.15s ease;
  transform:translate(-50%,-50%);
  mix-blend-mode: overlay;
}

/* 滚动渐入动画 - 高级动画 */
.fade-in {
  opacity: 0;
  transform: translateY(30px);
  transition: all 0.8s cubic-bezier(0.4, 0, 0.2, 1);
}
.fade-in.active {
  opacity: 1;
  transform: translateY(0);
}

/* 自定义滚动条 - 升级 */
::-webkit-scrollbar {
  width: 10px;
  height: 10px;
}
::-webkit-scrollbar-track {
  background: var(--bg-card);
}
::-webkit-scrollbar-thumb {
  background: linear-gradient(135deg, var(--primary-dark), var(--primary));
  border-radius: 5px;
  border: 2px solid var(--bg-card);
}
::-webkit-scrollbar-thumb:hover {
  background: linear-gradient(135deg, var(--primary), var(--primary-light));
  box-shadow: 0 0 10px rgba(122,148,255,0.5);
}

/* 页脚 - 新增高级页脚 */
.footer {
  background: linear-gradient(135deg, var(--bg-card) 0%, var(--bg-dark) 100%);
  border-top: 1px solid var(--border-light);
  padding: 60px 0 30px;
  margin-top: 80px;
  backdrop-filter: blur(10px);
}
.footer-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 25px;
}
.footer-top {
  display: flex;
  flex-wrap: wrap;
  gap: 60px;
  margin-bottom: 40px;
}
.footer-col {
  flex: 1;
  min-width: 250px;
}
.footer-col h3 {
  font-size: 20px;
  color: var(--primary);
  margin-bottom: 25px;
  font-weight: 700;
}
.footer-links {
  display: flex;
  flex-direction: column;
  gap: 15px;
}
.footer-link {
  color: var(--text-tertiary);
  text-decoration: none;
  font-size: 16px;
  transition: var(--transition);
  display: flex;
  align-items: center;
  gap: 8px;
}
.footer-link:hover {
  color: var(--primary);
  transform: translateX(5px);
}
.footer-contact {
  display: flex;
  flex-direction: column;
  gap: 20px;
}
.contact-item {
  display: flex;
  align-items: flex-start;
  gap: 12px;
}
.contact-item i {
  color: var(--primary);
  font-size: 20px;
  margin-top: 2px;
}
.contact-text {
  color: var(--text-secondary);
  font-size: 16px;
  line-height: 1.6;
}
.footer-bottom {
  text-align: center;
  padding-top: 30px;
  border-top: 1px solid var(--border-light);
  color: var(--text-tertiary);
  font-size: 14px;
}
.social-links {
  display: flex;
  gap: 15px;
  margin-top: 25px;
}
.social-link {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background: rgba(122,148,255,0.1);
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--primary);
  font-size: 18px;
  transition: var(--transition);
  border: 1px solid var(--border-light);
}
.social-link:hover {
  background: var(--primary);
  color: white;
  transform: translateY(-5px);
  box-shadow: 0 0 15px rgba(122,148,255,0.6);
}

/* 回到顶部按钮 - 新增 */
.back-to-top {
  position: fixed;
  right: 40px;
  bottom: 120px;
  width: 70px;
  height: 70px;
  border-radius: 50%;
  background: rgba(10,16,40,0.8);
  color: var(--primary);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 28px;
  cursor: pointer;
  transition: var(--transition);
  z-index: 9998;
  border: 1px solid var(--border-light);
  opacity: 0;
  visibility: hidden;
}
.back-to-top.show {
  opacity: 1;
  visibility: visible;
}
.back-to-top:hover {
  background: var(--primary);
  color: white;
  box-shadow: 0 0 20px rgba(122,148,255,0.8);
}

/* 移动端适配 - 优化体验 */
@media (max-width: 768px) {
  /* 导航适配 */
  .nav-links {
    display: none;
  }
  .mobile-menu-btn {
    display: block;
  }
  /* 封面适配 */
  .cover{
    padding: 140px 20px 100px;
    margin-top: 70px;
  }
  .cover h1 {
    font-size: clamp(2rem, 8vw, 3rem);
  }
  .cover p {
    font-size: clamp(1rem, 4vw, 1.4rem);
  }
  .cover-tag {
    padding: 8px 18px;
    font-size: 14px;
    margin: 0 5px 8px;
  }
  /* 页面板块适配 */
  .page {
    padding: 40px 25px;
    margin: 30px 0;
  }
  /* 数据卡片适配 */
  .stats-item {
    width: 100%;
    max-width: 240px;
  }
  /* TikTok优势图片网格适配 */
  .tiktok-advantage-grid {
    grid-template-columns: 1fr;
    gap: 20px;
  }
  /* 多图适配 */
  .multi-img-box {
    flex-direction: column;
  }
  .multi-img-item {
    min-width: 100%;
    height: 220px;
  }
  /* 团队卡片适配 */
  .team-item {
    width: 100%;
  }
  /* 轮播图适配 */
  .slider-box {
    height: 300px;
  }
  .slider-arrow {
    width: 40px;
    height: 40px;
    font-size: 20px;
  }
  /* 画廊适配 */
  .gallery-box {
    grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
  }
  .gallery-item {
    height: 180px;
  }
  /* 优势卡片适配 */
  .advantage-item {
    min-width: 100%;
  }
  /* 按钮适配 */
  .btn {
    padding: 16px 40px;
    font-size: 16px;
  }
  /* 悬浮按钮适配 */
  .float-btn, .back-to-top {
    width: 60px;
    height: 60px;
    font-size: 24px;
    right: 20px;
  }
  .float-btn {
    bottom: 20px;
  }
  .back-to-top {
    bottom: 90px;
  }
  /* 页脚适配 */
  .footer-top {
    gap: 40px;
  }
}
</style>
</head>

<body>
<!-- 粒子背景 -->
<div id="particles-js"></div>

<!-- 鼠标光效 -->
<div class="cursor-light"></div>

<!-- 导航栏 -->
<nav class="navbar" id="navbar">
  <div class="navbar-container">
    <a href="#" class="logo">
      <i class="fas fa-globe-asia"></i>
      全晟傳媒
    </a>
    <div class="nav-links">
      <a href="#home" class="nav-link">首頁</a>
      <a href="#advantage" class="nav-link">核心優勢</a>
      <a href="#why" class="nav-link">為什麼選擇我們</a>
      <a href="#company" class="nav-link">關於我們</a>
      <a href="#partner" class="nav-link">合作夥伴</a>
      <a href="#value" class="nav-link">核心價值</a>
      <a href="#tour" class="nav-link">旅行團實拍</a>
    </div>
    <div class="mobile-menu-btn">
      <i class="fas fa-bars"></i>
    </div>
  </div>
</nav>

<!-- 悬浮按钮 -->
<div class="float-btn">📞</div>

<!-- 回到顶部按钮 -->
<div class="back-to-top" id="backToTop">
  <i class="fas fa-arrow-up"></i>
</div>

<!-- 主容器 -->
<div class="container">
  <!-- 封面板块 -->
  <div class="cover" id="home">
    <div class="cover-content">
      <h1>TikTok旅行推廣 開啟流量變現新賽道</h1>
      <p>低門檻 · 高收益 · 全球流量 · 旅遊行業新機遇</p>
      <div>
        <span class="cover-tag">全球10億+流量池</span>
        <span class="cover-tag">AI智能創作</span>
        <span class="cover-tag">高佣金分成</span>
      </div>
    </div>
  </div>

  <!-- 核心優勢板塊 -->
  <div class="page" id="advantage">
    <div class="page-content">
      <h2 class="title">TikTok旅行推廣 核心優勢</h2>
      <div class="stats-box">
        <div class="stats-item fade-in">
          <div class="stats-num" id="num1">28</div>
          <div class="stats-text">百萬粉旅行賬號孵化</div>
        </div>
        <div class="stats-item fade-in">
          <div class="stats-num" id="num2">5000</div>
          <div class="stats-text">爆款影片單條播放(萬+)</div>
        </div>
        <div class="stats-item fade-in">
          <div class="stats-num" id="num3">18800</div>
          <div class="stats-text">創作者月均收益(元)</div>
        </div>
        <div class="stats-item fade-in">
          <div class="stats-num" id="num4">90%</div>
          <div class="stats-text">獲客成本降低率</div>
        </div>
      </div>
      
      <!-- TikTok核心优势图片网格 - 替换为新图片 -->
      <div class="tiktok-advantage-grid fade-in">
        <div class="tiktok-advantage-item">
          <img src="https://p3-flow-imagex-download-sign.byteimg.com/tos-cn-i-a9rns2rl98/e742db4da231446b9e3047efbfaef8d2.png~tplv-a9rns2rl98-24:720:720.png?lk3s=8e244e95&rcl=202604141002459169E5885B412D10CF47&rrcfp=8a172a1a&x-expires=1776736966&x-signature=ZYf%2Fd8z6%2B4CY1oIf%2Fsjl54lT21U%3D" alt="精准推荐算法：让对的内容找到对的人" loading="lazy">
        </div>
        <div class="tiktok-advantage-item">
          <img src="https://p26-flow-imagex-download-sign.byteimg.com/tos-cn-i-a9rns2rl98/cac8ef1d082045138625dfe762b87762.png~tplv-a9rns2rl98-24:720:720.png?lk3s=8e244e95&rcl=202604141002459169E5885B412D10CF47&rrcfp=8a172a1a&x-expires=1776736966&x-signature=OogVv8dDJ3%2FGa3h5au7aV%2FcOtns%3D" alt="沉浸式内容形式：旅行的最佳表达" loading="lazy">
        </div>
        <div class="tiktok-advantage-item">
          <img src="https://p3-flow-imagex-download-sign.byteimg.com/tos-cn-i-a9rns2rl98/ff74761280ea460cba0c320cc82cbdfe.png~tplv-a9rns2rl98-24:720:720.png?lk3s=8e244e95&rcl=202604141002459169E5885B412D10CF47&rrcfp=8a172a1a&x-expires=1776736966&x-signature=qe7GBg9q4SkJZjFZWobU7ITtLLs%3D" alt="无与伦比的用户覆盖与高粘性" loading="lazy">
        </div>
      </div>
      
      <!-- 删除了多图展示部分 -->
    </div>
  </div>

  <!-- 為什麼選擇TikTok -->
  <div class="page" id="why">
    <div class="page-content">
      <h2 class="title">為什麼選擇TikTok做旅行推廣？</h2>
      <div class="img-box fade-in">
        <img src="https://picsum.photos/id/25/1600/800" alt="TikTok旅行推廣優勢">
      </div>
      
      <!-- 删除了热门旅行推广场景和对应的图片画廊 -->
      
      <div class="benefit-desc fade-in">
        <p>✅ <strong>流量紅利巨大</strong>：TikTok全球月活超10億，旅行內容天然契合短影片傳播形式，曝光量是傳統渠道的10倍以上</p>
        <p>✅ <strong>變現效率高</strong>：旅遊產品佣金分成比例高，短影片種草轉化路徑短，用戶決策週期比圖文平台縮短60%</p>
        <p>✅ <strong>創作門檻低</strong>：無需親自出行，AI工具一鍵生成高品質旅遊素材，零基礎也能製作爆款影片</p>
        <p>✅ <strong>受眾精準</strong>：平台演算法精準匹配旅遊興趣用戶，推廣觸達率比傳統廣告提升80%，獲客成本大幅降低</p>
        <p>✅ <strong>全球化市場</strong>：突破地域限制，可觸達全球旅遊愛好者，單賬號可覆蓋多個國家和地區的旅遊推廣需求</p>
        <p>✅ <strong>持續性收益</strong>：優質旅遊內容可長期獲得流量收益，一次創作多次變現，形成穩定的被動收入</p>
      </div>
    </div>
  </div>

  <!-- 公司介紹板塊 -->
  <div class="page" id="company">
    <div class="page-content">
      <h2 class="title">關於我們 - 全晟傳媒</h2>
      <div class="img-box fade-in">
        <img src="https://picsum.photos/id/60/1600/800" alt="全晟傳媒公司介紹">
      </div>
      <div class="company-desc fade-in">
        <p>全晟傳媒是國內領先的TikTok跨境內容運營服務商，專注於旅遊垂類內容孵化與商業變現，擁有5年TikTok運營經驗和專業的內容創作團隊。</p>
        <p>我們深耕旅遊行業數位化營銷，累計服務超2000家旅遊商家，孵化出28個百萬粉絲級旅行賬號，打造了5000+爆款旅遊短影片，幫助創作者實現穩定的流量收益和推廣佣金。</p>
        <p>公司核心團隊均來自頭部MCN機構和旅遊行業龍頭企業，具備豐富的內容創作、賬號運營、商業變現經驗，為合作夥伴提供從內容創作到流量變現的全流程解決方案。</p>
      </div>
      
      <!-- 核心團隊展示 -->
      <div class="team-box fade-in">
        <div class="team-item">
          <div class="team-avatar">
            <svg width="60" height="60" viewBox="0 0 24 24" fill="#fff">
              <path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"/>
            </svg>
          </div>
          <h3>王總監</h3>
          <p>前TikTok官方運營專家</p>
          <p>8年跨境內容運營經驗</p>
        </div>
        <div class="team-item">
          <div class="team-avatar">
            <svg width="60" height="60" viewBox="0 0 24 24" fill="#fff">
              <path d="M21 16v-2l-8-5V3.5c0-.83-.67-1.5-1.5-1.5S10 2.67 10 3.5V9l-8 5v2l8-2.5V19l-2 1.5V22l3.5-1 3.5 1v-1.5L13 19v-5.5l8 2.5z"/>
            </svg>
          </div>
          <h3>李經理</h3>
          <p>旅遊行業營銷專家</p>
          <p>服務超800家旅遊商家</p>
        </div>
        <div class="team-item">
          <div class="team-avatar">
            <svg width="60" height="60" viewBox="0 0 24 24" fill="#fff">
              <path d="M12 10.9c-.61 0-1.1.49-1.1 1.1s.49 1.1 1.1 1.1c.61 0 1.1-.49 1.1-1.1s-.49-1.1-1.1-1.1zM12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm2.19 12.19L6 18l3.81-8.19L18 6l-3.81 8.19z"/>
            </svg>
          </div>
          <h3>張編導</h3>
          <p>爆款影片創作總監</p>
          <p>打造3000+百萬播放影片</p>
        </div>
      </div>
      
      <!-- 删除了公司环境展示图部分 -->
    </div>
  </div>

  <!-- 合作公司展示 -->
  <div class="page" id="partner">
    <div class="page-content">
      <h2 class="title">戰略合作企業</h2>
      <!-- 修改：替换为春辉旅游logo图片 -->
      <div class="img-box fade-in">
        <img src="https://p26-flow-imagex-download-sign.byteimg.com/tos-cn-i-a9rns2rl98/68073298c2164810ba9766cd21afe24c.png~tplv-a9rns2rl98-24:720:720.png?lk3s=8e244e95&rcl=20260414095233FE7080DE3B949BE7465C&rrcfp=8a172a1a&x-expires=1776736354&x-signature=OPVQhM%2FAQvNZxMaDOyRjKOTv8i0%3D" alt="春辉旅游" onerror="this.src='https://picsum.photos/1600/800'; this.alt='春辉旅游';">
      </div>
      <div class="partner-box fade-in">
        <div class="partner-item">
          <div class="partner-name">福建春輝旅集團有限公司</div>
        </div>
        <div class="partner-item">
          <div class="partner-name">聖達旅行社股份有限公司</div>
        </div>
        <div class="partner-item">
          <div class="partner-name">廈門海緣之旅國際旅行社</div>
        </div>
        <div class="partner-item">
          <div class="partner-name">台灣聖達旅行社</div>
        </div>
      </div>
      
      <div class="desc fade-in" style="margin-top:20px;">
        <p>我們與兩岸頂尖旅遊平台達成深度戰略合作，擁有豐富的旅遊產品資源和獨家佣金政策</p>
        <p>為創作者提供高分成、高轉化的旅遊推廣產品，為商家提供精準的流量曝光和客戶轉化</p>
      </div>
    </div>
  </div>

  <!-- 核心價值板塊 -->
  <div class="page" id="value">
    <div class="page-content">
      <h2 class="title">TikTok旅行推廣 核心價值</h2>
      <!-- 替换为用户提供的TikTok图片 -->
      <div class="img-box fade-in">
        <img src="https://p11-flow-imagex-download-sign.byteimg.com/tos-cn-i-a9rns2rl98/8e4377d8d84041979e11d6fd252f2efd.png~tplv-a9rns2rl98-24:720:720.png?lk3s=8e244e95&rcl=2026041409280461CA5CCF20E30B5241DB&rrcfp=8a172a1a&x-expires=1776734885&x-signature=RxBJ4EEcUc6Jql1u6jMmo8VBqlM%3D" alt="TikTok旅行推廣價值" onerror="this.src='https://picsum.photos/1600/800'; this.alt='TikTok旅行推廣價值';">
      </div>
      <div class="advantage-box fade-in">
        <div class="advantage-item">
          <h3>對創作者的價值</h3>
          <p>📱 零成本創業：無需囤貨、無需門店，一部手機即可開啟創作</p>
          <p>💰 多維度收益：流量收益+推廣佣金+平台補貼，收益來源多元</p>
          <p>📈 快速成長：7天掌握爆款創作邏輯，零基礎也能快速起號變現</p>
          <p>🌍 時間自由：不受地域和時間限制，隨時隨地創作變現</p>
        </div>
        <div class="advantage-item">
          <h3>對旅遊商家的價值</h3>
          <p>🚀 獲客成本低：相比傳統推廣渠道，獲客成本降低60%-80%</p>
          <p>📊 轉化效果好：短影片沉浸式體驗，用戶下單轉化率提升50%</p>
          <p>🌐 品牌曝光廣：觸達傳統渠道無法覆蓋的年輕消費群體</p>
          <p>📝 數據可追蹤：推廣效果實時監控，精準優化推廣策略</p>
        </div>
        <div class="advantage-item">
          <h3>行業發展優勢</h3>
          <p>📅 市場風口：2026年TikTok旅遊內容進入爆發期，競爭小機會大</p>
          <p>🤖 AI賦能：AI素材製作大幅提升創作效率，降低人力成本</p>
          <p>🌏 全球化布局：單賬號可覆蓋全球旅遊市場，收益空間無限</p>
          <p>📌 政策支持：平台大力扶持旅遊垂類內容，流量傾斜明顯</p>
        </div>
      </div>
    </div>
  </div>

  <!-- ✅ 新增：旅行團實拍展示板塊 -->
  <div class="page" id="tour">
    <div class="page-content">
      <h2 class="title">旅行團實拍展示</h2>
      <div class="desc fade-in">
        <p>真實出團記錄，專業導遊帶隊，品質服務全程保障，讓每一位旅客都能擁有完美的旅行體驗</p>
      </div>
      
      <!-- 旅行團照片網格 - 替换为用户提供的6张照片 -->
      <div class="gallery-box fade-in">
        <div class="gallery-item">
          <img src="https://p3-flow-imagex-download-sign.byteimg.com/tos-cn-i-a9rns2rl98/6f30f85234c1421eb84b44b2c41f8667.png~tplv-a9rns2rl98-24:720:720.png?lk3s=8e244e95&rcl=2026041409202444DCA8170DE892644D12&rrcfp=8a172a1a&x-expires=1776734425&x-signature=%2FhGWyvrPiwSnrEhIepTpFho1G4Q%3D" alt="旅行團出團合影">
        </div>
        <div class="gallery-item">
          <img src="https://p26-flow-imagex-download-sign.byteimg.com/tos-cn-i-a9rns2rl98/e0ff5ddf08c240eabcdb72ecb2b4e95e.png~tplv-a9rns2rl98-24:720:720.png?lk3s=8e244e95&rcl=2026041409202444DCA8170DE892644D12&rrcfp=8a172a1a&x-expires=1776734425&x-signature=G1JMaNlIC%2FR1IuCRONiEdFIyvYw%3D" alt="兩岸一家親出發機場">
        </div>
        <div class="gallery-item">
          <img src="https://p26-flow-imagex-download-sign.byteimg.com/tos-cn-i-a9rns2rl98/d98d62026a214c2e84d24bfe7ac65341.png~tplv-a9rns2rl98-24:720:720.png?lk3s=8e244e95&rcl=2026041409202444DCA8170DE892644D12&rrcfp=8a172a1a&x-expires=1776734425&x-signature=a4dgWwG8Y5oWWgsC%2FIkMj%2FA6nhU%3D" alt="團員互動合影">
        </div>
        <div class="gallery-item">
          <img src="https://p3-flow-imagex-download-sign.byteimg.com/tos-cn-i-a9rns2rl98/b0253c7d496c4a10a01209dd45a82294.png~tplv-a9rns2rl98-24:720:720.png?lk3s=8e244e95&rcl=2026041409202444DCA8170DE892644D12&rrcfp=8a172a1a&x-expires=1776734425&x-signature=ricQgIT6FPE3AxHUA9UVuz1J5OI%3D" alt="古鎮遊玩合影">
        </div>
        <div class="gallery-item">
          <img src="https://p26-flow-imagex-download-sign.byteimg.com/tos-cn-i-a9rns2rl98/6612e387482940b59682de2731879dbd.png~tplv-a9rns2rl98-24:720:720.png?lk3s=8e244e95&rcl=2026041409202444DCA8170DE892644D12&rrcfp=8a172a1a&x-expires=1776734425&x-signature=4rkX29xIFmyYezQtX%2F4ZcUXM0EM%3D" alt="特色美食體驗">
        </div>
        <div class="gallery-item">
          <img src="https://p26-flow-imagex-download-sign.byteimg.com/tos-cn-i-a9rns2rl98/790a7b5bdb654004aec139baffc7cc0b.png~tplv-a9rns2rl98-24:720:720.png?lk3s=8e244e95&rcl=2026041409202444DCA8170DE892644D12&rrcfp=8a172a1a&x-expires=1776734425&x-signature=Qy7jZqkX7tRzJD%2FyrzPhwGw3j58%3D" alt="景點參觀合影">
        </div>
      </div>

      <!-- 旅行團輪播圖 - 替换为用户提供的照片（取前4张） -->
      <div class="slider-box fade-in" style="margin-top:40px;">
        <div class="slider-container" id="tourSlider">
          <div class="slider-item">
            <img src="https://p3-flow-imagex-download-sign.byteimg.com/tos-cn-i-a9rns2rl98/6f30f85234c1421eb84b44b2c41f8667.png~tplv-a9rns2rl98-24:720:720.png?lk3s=8e244e95&rcl=2026041409202444DCA8170DE892644D12&rrcfp=8a172a1a&x-expires=1776734425&x-signature=%2FhGWyvrPiwSnrEhIepTpFho1G4Q%3D" alt="旅行團實拍1">
          </div>
          <div class="slider-item">
            <img src="https://p26-flow-imagex-download-sign.byteimg.com/tos-cn-i-a9rns2rl98/e0ff5ddf08c240eabcdb72ecb2b4e95e.png~tplv-a9rns2rl98-24:720:720.png?lk3s=8e244e95&rcl=2026041409202444DCA8170DE892644D12&rrcfp=8a172a1a&x-expires=1776734425&x-signature=G1JMaNlIC%2FR1IuCRONiEdFIyvYw%3D" alt="旅行團實拍2">
          </div>
          <div class="slider-item">
            <img src="https://p26-flow-imagex-download-sign.byteimg.com/tos-cn-i-a9rns2rl98/d98d62026a214c2e84d24bfe7ac65341.png~tplv-a9rns2rl98-24:720:720.png?lk3s=8e244e95&rcl=2026041409202444DCA8170DE892644D12&rrcfp=8a172a1a&x-expires=1776734425&x-signature=a4dgWwG8Y5oWWgsC%2FIkMj%2FA6nhU%3D" alt="旅行團實拍3">
          </div>
          <div class="slider-item">
            <img src="https://p3-flow-imagex-download-sign.byteimg.com/tos-cn-i-a9rns2rl98/b0253c7d496c4a10a01209dd45a82294.png~tplv-a9rns2rl98-24:720:720.png?lk3s=8e244e95&rcl=2026041409202444DCA8170DE892644D12&rrcfp=8a172a1a&x-expires=1776734425&x-signature=ricQgIT6FPE3AxHUA9UVuz1J5OI%3D" alt="旅行團實拍4">
          </div>
        </div>
        <div class="slider-arrow slider-prev" onclick="prevTourSlide()">◀</div>
        <div class="slider-arrow slider-next" onclick="nextTourSlide()">▶</div>
        <div class="slider-nav">
          <div class="slider-dot active" onclick="goToTourSlide(0)"></div>
          <div class="slider-dot" onclick="goToTourSlide(1)"></div>
          <div class="slider-dot" onclick="goToTourSlide(2)"></div>
          <div class="slider-dot" onclick="goToTourSlide(3)"></div>
        </div>
      </div>
    </div>
  </div>

  <!-- 黃金機遇 -->
  <div class="page" style="text-align:center">
    <div class="page-content">
      <h2 class="title">TikTok旅行推廣 黃金機遇</h2>
      <div class="img-box fade-in">
        <img src="https://picsum.photos/id/110/1600/800" alt="黃金機遇">
      </div>
      <div class="desc fade-in" style="font-size:18px;line-height:2.2;margin:30px 0;">
        <p>2026年是TikTok旅遊內容的黃金發展期，平台流量紅利+旅遊行業復甦+AI技術賦能</p>
        <p>抓住這波機遇，無論是個人創作者還是旅遊商家，都能在TikTok上實現流量和收益的雙重增長</p>
        <p>無需複雜的操作，無需高昂的成本，只需借助TikTok的流量優勢和專業的運營方法</p>
        <p>就能輕鬆打開旅行推廣的新市場，實現低風險、高回報的商業價值！</p>
      </div>

      <a href="#" class="btn">瞭解更多TikTok旅行推廣詳情</a>
    </div>
  </div>

</div>

<!-- 页脚 -->
<footer class="footer">
  <div class="footer-container">
    <div class="footer-top">
      <div class="footer-col">
        <h3>快速導航</h3>
        <div class="footer-links">
          <a href="#home" class="footer-link"><i class="fas fa-home"></i> 首頁</a>
          <a href="#advantage" class="footer-link"><i class="fas fa-star"></i> 核心優勢</a>
          <a href="#why" class="footer-link"><i class="fas fa-question-circle"></i> 為什麼選擇我們</a>
          <a href="#company" class="footer-link"><i class="fas fa-building"></i> 關於我們</a>
          <a href="#partner" class="footer-link"><i class="fas fa-handshake"></i> 合作夥伴</a>
          <a href="#tour" class="footer-link"><i class="fas fa-map-marked-alt"></i> 旅行團實拍</a>
        </div>
      </div>
      <div class="footer-col">
        <h3>聯繫我們</h3>
        <div class="footer-contact">
          <!-- 修改1：替换邮箱 -->
          <div class="contact-item">
            <i class="fas fa-envelope"></i>
            <div class="contact-text">郵箱：tomlaohu@gmail.com</div>
          </div>
          <!-- 修改2：新增LINE联系方式 -->
          <div class="contact-item">
            <i class="fab fa-line"></i>
            <div class="contact-text">LINE：qs555</div>
          </div>
          <!-- 修改3：保留地址，如需修改可自行调整 -->
          <div class="contact-item">
            <i class="fas fa-map-marker-alt"></i>
            <div class="contact-text">地址：福建省廈門市思明區觀音山商務中心</div>
          </div>
        </div>
        <div class="social-links">
          <a href="#" class="social-link"><i class="fab fa-weixin"></i></a>
          <a href="#" class="social-link"><i class="fab fa-weibo"></i></a>
          <a href="#" class="social-link"><i class="fab fa-tiktok"></i></a>
          <a href="#" class="social-link"><i class="fab fa-instagram"></i></a>
          <!-- 新增LINE图标 -->
          <a href="#" class="social-link"><i class="fab fa-line"></i></a>
        </div>
      </div>
      <div class="footer-col">
        <h3>服務承諾</h3>
        <div class="footer-links">
          <a href="#" class="footer-link"><i class="fas fa-shield-alt"></i> 7×24小時服務</a>
          <a href="#" class="footer-link"><i class="fas fa-chart-line"></i> 效果保障</a>
          <a href="#" class="footer-link"><i class="fas fa-money-bill-wave"></i> 無效退款</a>
          <a href="#" class="footer-link"><i class="fas fa-user-secret"></i> 隱私保護</a>
        </div>
      </div>
    </div>
    <div class="footer-bottom">
      <p>© 2026 全晟傳媒 版權所有 | 閩ICP備XXXXXXXX號</p>
    </div>
  </div>
</footer>

<script>
// 容错处理：如果外部库加载失败，定义空函数避免报错
if (typeof particlesJS === 'undefined') {
  window.particlesJS = function() {};
}
if (typeof CountUp === 'undefined') {
  window.CountUp = function() {
    this.start = function() {};
  };
}

// 粒子背景初始化
particlesJS('particles-js', {
  particles: {
    number: { value: 100, density: { enable: true, value_area: 800 } },
    color: { value: '#7a94ff' },
    shape: { type: 'circle' },
    opacity: { value: 0.6, random: true },
    size: { value: 4, random: true },
    line_linked: { enable: true, distance: 160, color: '#7a94ff', opacity: 0.3, width: 1.2 },
    move: { enable: true, speed: 1.2, direction: 'none', random: true, straight: false, out_mode: 'out', bounce: false }
  },
  interactivity: {
    detect_on: 'canvas',
    events: {
      onhover: { enable: true, mode: 'grab' },
      onclick: { enable: true, mode: 'push' },
      resize: true
    },
    modes: {
      grab: { distance: 150, line_linked: { opacity: 0.6 } },
      push: { particles_nb: 5 }
    }
  },
  retina_detect: true
});

// 数字计数动画
window.addEventListener('load', function() {
  try {
    const num1 = new CountUp('num1', 0, 28, 0, 3);
    const num2 = new CountUp('num2', 0, 5000, 0, 3);
    const num3 = new CountUp('num3', 0, 18800, 0, 3);
    const num4 = new CountUp('num4', 0, 90, 0, 3);
    num1.start();
    num2.start();
    num3.start();
    num4.start();
  } catch (e) {
    // 如果CountUp加载失败，直接显示静态数字
    document.getElementById('num1').textContent = '28';
    document.getElementById('num2').textContent = '5000';
    document.getElementById('num3').textContent = '18800';
    document.getElementById('num4').textContent = '90%';
  }

  // 图片加载处理
  document.querySelectorAll('img').forEach(img => {
    img.onload = function() {
      this.classList.add('loaded');
    };
    img.onerror = function() {
      this.style.display = 'none';
      this.parentElement.innerHTML = '<div style="padding:20px;text-align:center;">圖片加載失敗</div>';
    };
  });
});

// 鼠标光效
try {
  const cursorLight = document.querySelector('.cursor-light');
  document.addEventListener('mousemove', function(e) {
    if (cursorLight) {
      cursorLight.style.left = e.clientX + 'px';
      cursorLight.style.top = e.clientY + 'px';
    }
  });
} catch (e) {}

// 悬浮按钮点击事件
try {
  const floatBtn = document.querySelector('.float-btn');
  floatBtn.addEventListener('click', function() {
    // 修改4：悬浮按钮点击提示信息更新
    alert('立即諮詢TikTok旅行推廣詳情：\n郵箱：tomlaohu@gmail.com\nLINE：qs555');
  });
} catch (e) {}

// 滚动渐入动画
function checkFade() {
  const fadeElements = document.querySelectorAll('.fade-in');
  fadeElements.forEach(el => {
    const rect = el.getBoundingClientRect();
    const windowHeight = window.innerHeight;
    if (rect.top < windowHeight * 0.85 && rect.bottom > 0) {
      el.classList.add('active');
    }
  });
}

// 初始检查
checkFade();

// 滚动时检查
window.addEventListener('scroll', function() {
  checkFade();
  
  // 导航栏滚动效果
  const navbar = document.getElementById('navbar');
  if (window.scrollY > 50) {
    navbar.classList.add('navbar-scrolled');
  } else {
    navbar.classList.remove('navbar-scrolled');
  }
  
  // 回到顶部按钮显示/隐藏
  const backToTop = document.getElementById('backToTop');
  if (window.scrollY > 500) {
    backToTop.classList.add('show');
  } else {
    backToTop.classList.remove('show');
  }
});

// 回到顶部功能
document.getElementById('backToTop').addEventListener('click', function() {
  window.scrollTo({
    top: 0,
    behavior: 'smooth'
  });
});

// 轮播图功能 - 删除了原来的轮播图相关代码，只保留旅行团轮播

// 旅行團輪播控制
let tourSlideIndex = 0;
function updateTourSlider() {
  const slider = document.getElementById('tourSlider');
  const dots = document.querySelectorAll('#tour .slider-dot');
  slider.style.transform = `translateX(-${tourSlideIndex * 100}%)`;
  dots.forEach((dot, i) => dot.classList.toggle('active', i === tourSlideIndex));
}
function nextTourSlide() {
  tourSlideIndex = (tourSlideIndex + 1) % 4;
  updateTourSlider();
}
function prevTourSlide() {
  tourSlideIndex = (tourSlideIndex - 1 + 4) % 4;
  updateTourSlider();
}
function goToTourSlide(index) {
  tourSlideIndex = index;
  updateTourSlider();
}
// 自動輪播
setInterval(nextTourSlide, 6000);
</script>
</body>
</html>
