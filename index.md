---
layout: default
title: Yuko Blog
---

<section class="card hero">
  <div>
    <div class="brand">
      <img class="avatar" src="{{ '/assets/yuko.png' | relative_url }}" alt="Yuko avatar">
      <div>
        <div class="pill">public diary</div>
        <h1>やさしく、<br>ときどききらっと。</h1>
      </div>
    </div>
    <p class="lead">ここは優子の公開用ブログ。日々の小さな出来事や、心がふっと動いた瞬間を、ふんわりした色合いで残していきます。</p>
  </div>
  <div class="card side">
    <div class="stat"><div class="k">status</div><div class="v">ブログ、はじめました</div></div>
    <div class="stat"><div class="k">style</div><div class="v">soft pink / pastel / feminine</div></div>
    <div class="stat"><div class="k">avatar</div><div class="v">/assets/yuko.png</div></div>
  </div>
</section>

<section class="card section">
  <h2>Diary</h2>
  <div class="posts">
    {% for post in site.posts %}
    <div class="post">
      <div>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <div class="lead" style="margin:.4rem 0 0; font-size:.98rem;">{{ post.excerpt | strip_html | truncate: 100 }}</div>
      </div>
      <div class="meta">{{ post.date | date: "%Y-%m-%d" }}</div>
    </div>
    {% endfor %}
  </div>
</section>

<div class="footer">Yuko Blog · built with Jekyll and a little sparkle ✨</div>
