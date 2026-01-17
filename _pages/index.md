---
layout: page
title: Home
id: home
permalink: /
---
# Hola! 🐧

Este es un [[jardin digital]], un pequeño rincón del internet en el que yo tengo control total. Acá hay notas en progreso, comentarios, ensayos y algo de ficción propia (o lo habrá). Como mi mente, este es un lugar un poco desordenado y diverso, pero interconectado. Con ideas sobre pensamiento crítico, ciencia ficción, transhumanismo, tecnologías y escritura *per se*.


<strong>Notas actualizadas recientemente</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
