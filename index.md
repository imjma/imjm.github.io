---
layout: default
---

<header>
  <img id="avatar" class="avatar" src="/files/avatar.jpg" alt="{{ site.fullname }}">
  <h1>{{ site.fullname }}</h1>
  <p class="intro">Hi. I am a web developer from Shanghai, and I am working at Sydney now. I am also a <a href="https://www.facebook.com/mrmimage">photographer</a>.</p>
  <p>
    <a title="Twitter" href="http://twitter.com/imdecoder/"<i class="icon-twitter icon-2x icon-border"></i></a>
    <a title="Github" href="http://github.com/imdecoder/"<i class="icon-github icon-2x icon-border"></i></a>
    <a title="Weibo" href="http://weibo.com/kenziii/"<i class="icon-weibo icon-2x icon-border"></i></a>
    <a title="Flickr" href="http://www.flickr.com/photos/dakkon"<i class="icon-flickr icon-2x icon-border"></i></a>
    <a title="Facebook" href="https://www.facebook.com/jiema"<i class="icon-facebook-sign icon-2x icon-border"></i></a>
    <a title="Linkedin" href="http://au.linkedin.com/in/jiema"<i class="icon-linkedin icon-2x icon-border"></i></a>
  </p>
</header>
<hr>

{% for post in paginator.posts %}
  <article>
    <h3>
    {% if post.external-url %}
    <a title="{{ post.title }}" rel="bookmark" href="{{ post.url }}" class="permalink icon-link"></a>
    <a href="{{ post.external-url }}" title="{{ post.title }}" class="postTitle">{{ post.title }}</a>
    {% else %}
    <a href="{{ post.url }}" title="{{ post.title }}" class="postTitle shiftTitle" rel="bookmark">{{ post.title }}</a>
    {% endif %}
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}" class="meta">{{ post.date | date:"%d %B %Y" }}</time>
    </h3>
  </article>
{% endfor %}
<!-- Pagination links -->

<div class="pageNav">
  {% if paginator.previous_page %}
    <div class="prev"><a href="/{{ paginator.previous_page_path }}">Newer</a></div>
  {% endif %}
  {% if paginator.next_page %}
    <div class="next"><a href="/{{ paginator.next_page_path }}">Older</a></div>
  {% endif %}
</div>