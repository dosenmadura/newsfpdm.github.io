---
layout: default
title: Beranda
---

<section class="hero">

  <div class="hero-content">

    <span class="hero-label">PORTAL BERITA FPDM</span>

    <h1>Informasi, Kegiatan & Gagasan<br>Dosen Madura</h1>

    <p>
      Media informasi resmi Forum Profesi Dosen Madura.
      Menyajikan berita, kegiatan, opini, dan informasi akademik.
    </p>

  </div>

</section>


<section class="news-section">

  <div class="section-heading">

    <div>
      <span class="section-label">TERBARU</span>
      <h2>Berita Terbaru</h2>
    </div>

    <a href="/berita/">Lihat Semua →</a>

  </div>


  <div class="post-grid">

    {% for post in site.posts limit:6 %}

    <article class="news-card">

      <div class="news-card-content">

        <span class="post-date">
          {{ post.date | date: "%d %B %Y" }}
        </span>

        <h3>
          <a href="{{ post.url | relative_url }}">
            {{ post.title }}
          </a>
        </h3>

        <p>
          {{ post.excerpt | strip_html | truncate: 140 }}
        </p>

        <a class="read-more"
           href="{{ post.url | relative_url }}">
          Baca Selengkapnya →
        </a>

      </div>

    </article>

    {% endfor %}

  </div>

</section>
