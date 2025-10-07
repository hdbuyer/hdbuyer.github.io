---
layout: default
title: "首页"
---

<div class="company-intro">
  <h1 style="text-align: center; color: #d32f2f;">传承同仁堂精髓，创新健康产业</h1>
  <p style="font-size: 1.2em; line-height: 1.6; text-align: center;">
    自 <strong>2017年</strong> 扎根于金色德令哈，我们肩负着将青藏高原"<strong>净土、净水、净空、净心</strong>"孕育的特色生物资源，通过同仁堂 <strong>355年</strong> 的匠心工艺，惠及天下众生的使命。
  </p>
</div>

## 🎬 企业介绍视频

<div style="text-align: center; margin: 3rem 0;">
  <div class="video-container" style="max-width: 800px; margin: 0 auto; background: #000; border-radius: 8px; overflow: hidden; box-shadow: 0 10px 30px rgba(0,0,0,0.3); position: relative;">
    
    <!-- 视频封面图和播放按钮 -->
    <div id="video-poster" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; background: linear-gradient(rgba(211,47,47,0.1), rgba(211,47,47,0.1)), url('/assets/images/video-poster.jpg') center/cover; display: flex; align-items: center; justify-content: center; cursor: pointer; z-index: 2;">
      <div style="text-align: center; color: white;">
        <div style="font-size: 4rem; margin-bottom: 1rem; text-shadow: 0 2px 10px rgba(0,0,0,0.5);">▶</div>
        <h3 style="margin: 0; font-size: 1.5rem; text-shadow: 0 2px 4px rgba(0,0,0,0.5);">播放企业宣传片</h3>
        <p style="margin: 0.5rem 0 0 0; opacity: 0.9;">了解同仁堂健康药业的现代化生产基地</p>
      </div>
    </div>
    
    <!-- 视频播放器 - 使用您提供的URL -->
    <video 
      id="company-video"
      controls 
      width="100%" 
      preload="metadata"
      style="display: none; position: relative; z-index: 1;"
      poster="/assets/images/video-poster.jpg"
    >
      <source src="https://www.tongrentang.com/file/upload/jkqinghai.mp4" type="video/mp4">
      您的浏览器不支持 HTML5 视频播放，请 <a href="https://www.tongrentang.com/file/upload/jkqinghai.mp4" target="_blank" style="color: #d32f2f;">点击这里下载观看</a>。
    </video>
  </div>
  
  <p style="color: #666; margin-top: 1rem; font-size: 0.9rem;">
    点击播放，深入了解同仁堂健康药业（青海）的现代化生产基地与严格的质量控制流程
  </p>
</div>

<script>
// 视频播放控制 - 优化版本
document.addEventListener('DOMContentLoaded', function() {
    const video = document.getElementById('company-video');
    const poster = document.getElementById('video-poster');
    
    // 预加载视频元数据以提高响应速度
    if (video) {
        video.load();
    }
    
    if (poster && video) {
        poster.addEventListener('click', function() {
            // 隐藏封面，显示视频
            poster.style.display = 'none';
            video.style.display = 'block';
            
            // 尝试播放视频
            const playPromise = video.play();
            
            if (playPromise !== undefined) {
                playPromise.catch(function(error) {
                    console.log('视频播放失败:', error);
                    // 显示友好的错误信息
                    poster.innerHTML = `
                        <div style="text-align: center; color: white; padding: 2rem;">
                            <h3>视频播放遇到问题</h3>
                            <p>请尝试刷新页面或直接<a href="https://www.tongrentang.com/file/upload/jkqinghai.mp4" target="_blank" style="color: #ffcc00; text-decoration: underline;">下载视频</a>观看</p>
                            <button onclick="location.reload()" style="background: #d32f2f; color: white; border: none; padding: 10px 20px; border-radius: 4px; cursor: pointer; margin-top: 1rem;">重新加载</button>
                        </div>
                    `;
                    poster.style.display = 'flex';
                });
            }
        });
    }
    
    // 视频结束时显示封面图
    if (video) {
        video.addEventListener('ended', function() {
            poster.style.display = 'flex';
            video.style.display = 'none';
        });
        
        // 视频加载错误处理
        video.addEventListener('error', function(e) {
            console.log('视频加载错误:', e);
            poster.innerHTML = `
                <div style="text-align: center; color: white; padding: 2rem;">
                    <h3>视频加载失败</h3>
                    <p>网络连接问题或视频暂时不可用</p>
                    <button onclick="location.reload()" style="background: #d32f2f; color: white; border: none; padding: 10px 20px; border-radius: 4px; cursor: pointer; margin-top: 1rem;">重新加载</button>
                </div>
            `;
            poster.style.display = 'flex';
        });
    }
});

// 添加键盘支持 - 按空格键播放/暂停
document.addEventListener('keydown', function(e) {
    if (e.code === 'Space') {
        const video = document.getElementById('company-video');
        if (video && video.style.display === 'block') {
            e.preventDefault();
            if (video.paused) {
                video.play();
            } else {
                video.pause();
            }
        }
    }
});
</script>

## 🏔️ 我们的核心优势

<div class="feature-list">
  <div class="feature-item">
    <h3>🏭 现代化生产基地</h3>
    <p><strong>10万级洁净车间</strong>，6条现代化生产线，年产能达XX吨，确保每一件产品都符合最高质量标准。</p>
  </div>
  
  <div class="feature-item">
    <h3>🔬 严格质量体系</h3>
    <p>建立<strong>56道质检工序</strong>，第三方权威机构月度抽检，产品合格率持续保持100%。</p>
  </div>
  
  <div class="feature-item">
    <h3>🌿 青藏特色资源</h3>
    <p>深度开发冬虫夏草、黑枸杞、藜麦等<strong>青藏高原特有生物资源</strong>，原料溯源，品质保证。</p>
  </div>
  
  <div class="feature-item">
    <h3>🎯 专业研发团队</h3>
    <p>依托同仁堂强大的研发实力，拥有<strong>博士、硕士研发团队</strong>，不断创新产品配方和工艺。</p>
  </div>
</div>

## 💼 核心业务领域

<div class="product-grid">
  <div class="product-card">
    <h3>青藏特色健康产品</h3>
    <ul style="text-align: left;">
      <li>冬虫夏草系列</li>
      <li>黑果枸杞系列</li>
      <li>高原藜麦系列</li>
      <li>特色健康食品</li>
    </ul>
    <a href="/products" class="cta-button">查看产品</a>
  </div>
  
  <div class="product-card">
    <h3>OEM/ODM合作</h3>
    <ul style="text-align: left;">
      <li>配方定制开发</li>
      <li>包装一体化设计</li>
      <li>灵活生产订量</li>
      <li>资质文件支持</li>
    </ul>
    <a href="/contact" class="cta-button">合作咨询</a>
  </div>
  
  <div class="product-card">
    <h3>质量认证服务</h3>
    <ul style="text-align: left;">
      <li>ISO22000认证</li>
      <li>绿色食品认证</li>
      <li>有机产品认证</li>
      <li>出口资质备案</li>
    </ul>
    <a href="/about" class="cta-button">了解详情</a>
  </div>
</div>

## 🏛️ 企业文化传承

> "**炮制虽繁必不敢省人工，品味虽贵必不敢减物力**"
> 
> —— 同仁堂古训

<div style="background: #fff3e0; padding: 1.5rem; border-radius: 8px; margin: 2rem 0;">
  <h3 style="color: #d32f2f; margin-top: 0;">企业精神</h3>
  <p><strong>{{ site.corporate_spirit }}</strong></p>
  <p>我们恪守"{{ site.self_discipline }}"的自律意识，秉承"{{ site.product_tenet }}"的产品宗旨。</p>
</div>

## 📞 立即联系合作

<div style="text-align: center; background: #f8f9fa; padding: 2rem; border-radius: 8px;">
  <h3>开启健康产业合作新篇章</h3>
  <p>电话：<strong>{{ site.phone }}</strong></p>
  <p>邮箱：<strong>{{ site.email }}</strong></p>
  <p>地址：{{ site.location }}</p>
  <a href="/contact" class="cta-button">获取专业咨询</a>
</div>