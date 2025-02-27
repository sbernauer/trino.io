---
layout: default
title: Trino Community Broadcast
show_hero: true
---

<div class="container container__broadcast">
<div class="row spacer-60">
<div markdown="1" class="col-lg-8">

The Trino Community Broadcast is a show about the Trino project and community.
Topics include the data sources, clients, add-ons, platforms and usages of
Trino. We interview users, contributors, partners, and other community members
about their connection to Trino, look at demos together, and chat about the tech
stacks, the code, and often explain concepts along the way.

Each episode also brings you news about the latest releases, events, and
interesting developments in the ecosystem around Trino.

## Upcoming episodes

<dl>
<dt>22 Feb 2024: Trino Community Broadcast 56 - VAST</dt>
<dd>Colleen Tartow and Roman Zedgev from
<a href="../ecosystem/data-source.html#vast">VAST</a> chat with us
about the VAST Trino connector, Trino running on VAST compute, and some really
cool usage scenarios.</dd>

<dt>14 Mar 2024: Trino Community Broadcast 57 - OpenTelemetry</dt>
<dd>David Phillips and Matt Stephenson from Starburst join us to talk about
their work on adding
<a href="../ecosystem/add-on.html#opentelemetry">OpenTelemetry</a>
support to Trino. We will run a little demo and chat about usage of the
integration at scale for Starburst Galaxy.</dd>

<dt>4 Apr 2024: Trino Community Broadcast 58 - Mitzu</dt>
<dd>
István Mészáros chats about his company and analytics tool
<a href="../ecosystem/client.html#mitzu">Mitzu</a> - a friendly, no-code product
analytics tool for warehouse-first companies that supports Trino.</dd>
</dl>

Find [more details and other events on our calendar]({{site.url}}/community.html#events).

Trino users, contributors, and partners, we want to hear from you! If you have a
topic, question or pull request that you would like us to feature on the show
join the [Trino slack]({{site.url}}/slack) and contact us there.




</div>
<div markdown="1" class="col-lg-3">

## Hosts

- Brian Olsen [@bitsondatadev](https://twitter.com/bitsondatadev)
- [Cole Bowden](https://www.linkedin.com/in/cole-m-bowden)
- Manfred Moser [@simpligility](https://twitter.com/simpligility)

## Watch or listen

- Watch:
<a href="https://www.youtube.com/playlist?list=PLFnr63che7war_NzC7CJQjFuUKLYC7nYh" target="_blank">
  <i class="fab fa-youtube watch-listen-icon" title="Youtube"></i>
</a>
<a href="https://www.twitch.tv/trinodb" target="_blank">
  <i class="fab fa-twitch watch-listen-icon" title="Twitch"></i>
</a>
- Listen:
<a href="https://podcasts.apple.com/us/podcast/trino-community-broadcast/id1533484786" target="_blank">
  <i class="fab fa-apple watch-listen-icon" title="Apple"></i>
</a>
<a href="https://podcasts.google.com/feed/aHR0cHM6Ly9mYXN0Lndpc3RpYS5jb20vY2hhbm5lbHMvN2Z1dzA0czd2Yy9yc3M" target="_blank">
  <i class="fab fa-google watch-listen-icon" title="Google"></i>
</a>
<a href="https://open.spotify.com/show/53ZrVCCmZSsEmvlNfzpWSL" target="_blank">
  <i class="fab fa-spotify watch-listen-icon" title="Spotify"></i>
</a>
- <a href="{{ '/broadcast/feed.xml' | relative_url }}">Subscribe via RSS</a>

</div>
<div markdown="1" class="col-md-12">

## Latest episode

{% assign latestEpisode =  site.episodes | last %}

<div class="post-entry card latest-entry">
  <div class="d-flex flex-column-reverse flex-lg-row justify-content-between">
    <div class="latest-entry-text-container">
      <h3><a class="post-link" href="{{ latestEpisode.url | relative_url }}">{{ latestEpisode.title | escape }}</a></h3>
      <span class="post-meta">{{ latestEpisode.date | date: "%b %-d, %Y" }}</span>
      <ul>
        {% for section in latestEpisode.sections %}
        <li>
            {{section.title}}:
            <a href="https://www.youtube.com/watch?v={{ latestEpisode.youtube_id}}&t={{ section.time }}s" target="_blank">
            {{ section.desc }}
            </a>
        </li>
        {% endfor %}
      </ul>
      <a href="{{ site.baseurl }}{{ latestEpisode.url }}" style="margin-top: auto;">Listen, watch, or read the show notes...</a>
    </div>
    <div class="latest-entry-video-container">
        <div class="latest-entry-video-wrapper">
          <iframe src="https://www.youtube.com/embed/{{ latestEpisode.youtube_id }}" frameborder="0" allowfullscreen></iframe>
        </div>
    </div>
  </div>
</div>

<div markdown="1" class="previous-episode-header">

## Previous episodes

<a href="/broadcast/episodes.html">See all episodes</a>
</div>
<div class="episode-grid">
{% assign offsetNumber = site.episodes.size | minus: 10 %}
{% for episode in site.episodes reversed offset:offsetNumber %}
{% if forloop.first == true %}
 {% continue %}
{% else %}
  <div class="post-entry card">
    <h5><a class="post-link" href="{{ episode.url | relative_url }}">{{ episode.title | escape }}</a></h5>
    <span class="post-meta">{{ episode.date | date: "%b %-d, %Y" }}</span>
    <ul>
      {% for section in episode.sections limit:3 %}
      <li>
          {{section.title}}:
          <a href="https://www.youtube.com/watch?v={{ episode.youtube_id}}&t={{ section.time }}s" target="_blank">
          {{ section.desc }}
          </a>
      </li>
      {% endfor %}
    </ul>
    <a href="{{ site.baseurl }}{{ episode.url }}">Listen, watch, or read the show notes...</a>
  </div>
{% endif %}
{% endfor %}
</div>

</div>
</div>
</div>
