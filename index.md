----
layout: default
title: "Home"
---

<section class="hero">

  <span class="eyebrow">
    Research Journal
  </span>

  <h1>
    Ideas worth
    <span>exploring.</span>
  </h1>

  <p class="hero-copy">
    Research, projects, and ideas from a student developer.
  </p>

  <div class="hero-actions">

    <a
      class="button button-primary"
      href="#latest"
    >
      Read my research
    </a>

    <a
      class="button button-ghost"
      href="{{ '/about/' | relative_url }}"
    >
      About me
    </a>

  </div>

</section>


<section
  class="section"
  id="latest"
>

  <div class="section-heading">

    <div>
      <span class="eyebrow">
        Latest
      </span>

      <h2>
        Research & writing
      </h2>
    </div>

  </div>


  <div class="post-grid">

    {% for post in site.posts %}

      <article class="post-card">

        <div class="post-card-top">

          <span class="tag">
            {{ post.category | default: "Research" }}
          </span>

          <span class="post-date">
            {{ post.date | date: "%b %-d, %Y" }}
          </span>

        </div>


        <h3>

          <a href="{{ post.url | relative_url }}">
            {{ post.title }}
          </a>

        </h3>


        <p>
          {{ post.description }}
        </p>


        <a
          class="text-link"
          href="{{ post.url | relative_url }}"
        >
          Read article
        </a>

      </article>

    {% endfor %}

  </div>

</section>