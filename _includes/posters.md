<h2 id="posters" style="margin: 2px 0px 10px;">Posters</h2>

{% assign posters = site.data.posters.main %}
{% if posters and posters.size > 0 %}
<div class="poster-list">
{% for poster in posters %}
<div class="poster-entry">
  <p class="poster-title"><strong>{{ poster.title }}</strong></p>
  <p class="poster-authors">{{ poster.authors }}</p>
  <p class="poster-info">
    <em>{{ poster.event }}</em>{% if poster.date %}, {{ poster.date }}{% endif %}
    {% if poster.pdf %}<a class="poster-pdf-link" href="{{ poster.pdf }}" target="_blank">PDF</a>{% endif %}
  </p>
</div>
{% endfor %}
</div>
{% else %}
<p>No posters yet. Add entries to <code>_data/posters.yml</code>.</p>
{% endif %}
