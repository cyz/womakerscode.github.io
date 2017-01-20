---
layout: default
title: 'WoMakersCode - Sobre'
description: Termo de Conduta de voluntários e participantes do projeto WoMakersCode, válido em todos os locais em que o projeto for implementado.
permalink: /agenda/
---

<section class="overview">
    <div class="container">
        <h1>Empoderar é o primeiro passo para novas revoluções</h1>
        <p class="text-justify">O WoMakersCode é um projeto livre, sem fins lucrativos, criado e mantido por voluntários, que almeja o empoderamento feminino, em especial na área de tecnologia. Empoderar é incentivar a participação, o aprendizado colaborativo e acima de tudo, dar voz às mulheres.</p>

    <h2><i class="fa fa--title fa-floppy-o" aria-hidden="true"></i>
Eventos anteriores</h2>
    {% for evento in site.data.agenda %}
      <article class="local-calendar"><h2>{{ evento.group }}</h2>
      {% for element in evento.elements %}

        <table class="table-calendar">
          <thead>
            <tr>
              <td><h3>{{ element.title }}</h3></td>
            </tr>
          </thead>
          <tbody>
          <tr>
            <td><i class="fa fa--agenda fa-calendar"></i> <b>Data:</b> <time datetime="{{ element.date }}">{{ element.date }}</time></td>
          </tr>
          <tr>
            <td><i class="fa fa--agenda fa-map-marker"></i> <b>Local:</b> {{ element.place }}</td>
          </tr>
          <tr>
            <td><i class="fa fa--agenda fa-certificate"></i> <b>Pré-requisito:</b>{{ element.complexity }}</td>
          </tr>
          <tr>
            <td><i class="fa fa--agenda fa-bullhorn"></i> <b>Organizador@s:</b> {{ element.organizer }}</td>
          </tr>
          <tr>
            <td>
              <p class="text-justify">{{ element.description }}</p>
              <p><a href="{{ element.link }}" target="_blank">Acesse a página desta atividade</a></p>
            </td>
          </tr>
        </tbody>
        </table>
      {% endfor %}
    </article>
    {% endfor %}

    </div>
</section>
