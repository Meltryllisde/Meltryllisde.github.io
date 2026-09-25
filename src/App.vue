<script setup lang="ts">
import profileImage from './assets/melt-1.png'

const publications = [
  {
    year: '2026',
    title: 'Pretext Reasoning: Scaling the Building Blocks of Interleaved Multimodal Reasoning',
    authors: 'Jiawei Gu, Linjie Li, Yiming Liu, Yunzhuo Hao, Zhichao Peng, Huichen Will Wang, Guanzheng Chen, Luxin Xu, Xinyu Zhang, Luo Li, Disen Lan, Zican Hu, Mingyang Song, David Valente, Alex Jinpeng Wang, Yafu Li, Ganqu Cui, Zhengyuan Yang, Michael Qizhe Shieh, Yejin Choi, Ranjay Krishna, Yu Cheng',
    href: '#',
  },
]
</script>

<template>
  <div class="site-shell">
    <header class="site-header">
      <a class="wordmark" href="#top" aria-label="Home">Inory<span>.</span></a>
      <nav aria-label="Primary navigation">
        <a href="#publications">Publications</a>
        <a href="#contact">Contact</a>
      </nav>
    </header>
    
    <main id="top">
      <section class="intro-section" aria-label="Introduction">
        <div class="intro-copy">
          <p class="intro-lead">
            <strong>About Me</strong>
          </p>
          <p class="intro-detail">
            I’m <strong>Zhichao Peng</strong>, a Master's student at the Central South University, advised by <a class="advisor-link" href="https://fingerrec.github.io/" target="_blank" rel="noreferrer"><strong>Prof. Alex Jinpeng Wang</strong><span>↗</span></a>. 
            <br />
            My research focuses on Multimodal Large Models and Embodied AI.
          </p>
          <div class="intro-links">
            <a href="mailto:inorymelt@gmail.com">Get in touch <span>↗</span></a>
            <a href="#publications">Read my work <span>↓</span></a>
          </div>
        </div>
        <div class="intro-aside" aria-label="Current position">
          <img class="profile-photo" :src="profileImage" alt="Zhichao Peng" />
          <span class="aside-label">Nick Name</span>
          <p>Inory</p>
          <span class="aside-label">Currently</span>
          <p>Master's Student<br />at the Central South University<br /> </p>
          <span class="aside-label">Based in</span>
          <p>China Hunan<br />Changsha</p>
        </div>
      </section>

      <section id="publications" class="publications-section">
        <div class="section-heading">
          <!-- <p class="eyebrow">Selected work</p> -->
          <h1>Publications</h1>
        </div>

        <div class="publication-list">
          <article v-for="publication in publications" :key="publication.title" class="publication-item">
            <div class="publication-year">{{ publication.year }}</div>
            <div class="publication-content">
              <h2><a :href="publication.href">{{ publication.title }} <span>↗</span></a></h2>
              <p class="publication-meta">{{ publication.authors }}<br /></p>
            </div>
          </article>
        </div>
      </section>
    </main>

    <footer id="contact" class="site-footer">
      <p>Have a chat, idea, or good book recommendation?</p>
      <a href="mailto:inorymelt@gmail.com">inorymelt@gmail.com <span>↗</span></a>
      <small>© {{ new Date().getFullYear() }} Inory</small>
    </footer>
  </div>
</template>
