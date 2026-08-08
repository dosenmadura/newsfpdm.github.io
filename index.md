---
layout: default
title: Beranda
---

<!-- HERO -->

<section class="hero">

  <div class="hero-text">

    <span class="hero-label">
      NEWS FPDM
    </span>

    <h1>
      Informasi, Kegiatan & Gagasan
      Dosen Madura
    </h1>

    <p>
      Portal berita resmi Forum Profesi Dosen Madura yang
      menyajikan informasi, kegiatan, opini dan perkembangan
      akademik di Madura.
    </p>

  </div>

</section>


<!-- BERITA UTAMA -->

<section class="news-section">

  <div class="section-title">

    <div>
      <span>BERITA UTAMA</span>
      <h2>Berita Terbaru</h2>
    </div>

    <a href="/berita/">
      Semua Berita →
    </a>

  </div>


  {% assign featured = site.posts.first %}

  {% if featured %}

  <div class="featured-news">

    <article class="featured-card">

      <div class="featured-image">

        {% if featured.image %}

        <img src="{{ featured.image }}" alt="{{ featured.title }}">

        {% else %}

        <div class="image-placeholder">
          NEWS FPDM
        </div>

        {% endif %}

      </div>


      <div class="featured-content">

        <span class="category">
          BERITA FPDM
        </span>

        <h2>
          <a href="{{ featured.url | relative_url }}">
            {{ featured.title }}
          </a>
        </h2>

        <div class="date">

          {{ featured.date | date: "%d %B %Y" }}

        </div>

        <p>
          {{ featured.excerpt | strip_html | truncate: 220 }}
        </p>

        <a class="read-button"
           href="{{ featured.url | relative_url }}">

          Baca Selengkapnya →

        </a>

      </div>

    </article>


    <!-- BERITA SAMPING -->

    <div class="side-news">

      {% for post in site.posts limit:3 offset:1 %}

      <article class="side-card">

        <div class="side-image">

          {% if post.image %}

          <img src="{{ post.image }}" alt="{{ post.title }}">

          {% else %}

          <div class="small-placeholder">
            FPDM
          </div>

          {% endif %}

        </div>

        <div class="side-content">

          <span class="category">
            BERITA
          </span>

          <h3>
            <a href="{{ post.url | relative_url }}">
              {{ post.title }}
            </a>
          </h3>

          <span class="date">
            {{ post.date | date: "%d %B %Y" }}
          </span>

        </div>

      </article>

      {% endfor %}

    </div>

  </div>

  {% endif %}

</section>


<!-- BERITA TERBARU -->

<section class="news-section">

  <div class="section-title">

    <div>
      <span>UPDATE</span>
      <h2>Berita Terbaru</h2>
    </div>

  </div>


  <div class="news-grid">

    {% for post in site.posts limit:9 %}

    <article class="news-box">

      <div class="news-image">

        {% if post.image %}

        <img src="{{ post.image }}" alt="{{ post.title }}">

        {% else %}

        <div class="image-placeholder">
          NEWS FPDM
        </div>

        {% endif %}

      </div>


      <div class="news-content">

        <span class="category">
          BERITA
        </span>

        <h3>

          <a href="{{ post.url | relative_url }}">

            {{ post.title }}

          </a>

        </h3>

        <div class="date">

          {{ post.date | date: "%d %B %Y" }}

        </div>

        <p>

          {{ post.excerpt | strip_html | truncate: 120 }}

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
