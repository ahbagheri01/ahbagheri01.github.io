<h2 id="highlighted-projects" style="margin: 2px 0px -15px;">Highlighted Projects</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.projects.main %}

<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    {% if link.image %}
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
    {% if link.badge %}
    <abbr class="badge">{{ link.badge }}</abbr>
    {% endif %}
    {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      {% if link.page or link.pdf %}
      <div class="title"><a href="{{ link.page | default: link.pdf }}">{{ link.title }}</a></div>
      {% else %}
      <div class="title">{{ link.title }}</div>
      {% endif %}
      <div class="author">{{ link.where }}</div>
      <div class="periodical"><em>{{ link.description }}</em></div>
    <div class="links">
      {% if link.pdf %}
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.page %}
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
    </div>
  </div>
</div>
</li>
<br>

{% endfor %}

</ol>
</div>
