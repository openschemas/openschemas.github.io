---
layout: default
title: Openschemas Specifications
permalink: specifications/
---
<h1>{{ site.name }} Specifications</h1>

<p>This page contains release versions of the Openschemas specifications. Ongoing changes are published via the <a href="/specifications/drafts">drafts</a> page. This page will be updated when the first drafts come through, and the continuous integration is built to integrate the specifications.</p>
<p>Should you wish to contact the community to discuss our efforts please post an issue on <a href="{{ site.repo }}" itemprop="email">the issues board</a>.</p>

<h2>Profiles</h2>

<p>The Openschemas' profiles define a community agreed layer over the Schema.org model providing additional constraints. These constraints capture (i) the information properties agreed by the community which are minimum (M), recommended (R), or optional (O), (ii) the cardinality of the property, i.e. whether it is expected to occur once or many times, and (iii) associated controlled vocabulary terms drawn from existing ontologies. </p>

<div class="bioschemas-spec-list-wrapper">
  <table class="bioschemas_spec_list" style="width: 100%; margin-left: auto; margin-right: auto; text-align: center;">
      <thead>
      <tr>
      <th>Name</th>
      <th style="text-align: center;">Group</th>
      <th style="text-align: center;">Use Cases</th>
      <th style="text-align: center;">Cross Walk</th>
      <th style="text-align: center;">Task &amp; Issues</th>
      <th style="text-align: center;">Examples</th>
      <th style="text-align: center;">Live Deploys</th>
      </tr>
      </thead>
      <tbody>
      {% assign prof_specs = site.specifications | where: 'spec_type', 'Profile'%}
      {% for spec in prof_specs %}
      <tr>
          {% assign date_time = spec.spec_info.version_date %}
          <th><a href="/specifications/{{spec.name}}" title="{{ spec.spec_info.subtitle }}">{{ spec.spec_info.title }}</a><br />(v{{spec.spec_info.version}})<br />{{ date_time | date_to_long_string }}</th>
          <td>
            {% assign group = site.groups | where:"identifier", spec.group %}
            {% for g in group %}
            <a href="{{g.url}}">{{g.name}}</a>
            {% endfor %}
          </td>
          <td class="spec_links">
            {% if spec.use_cases_url == '' %}
            <a>
            <img src="/images/use_case_spec.png" alt="View BioSchemas {{ spec.spec_info.title }} Use Cases"  style="filter: grayscale(100%);">
            </a>
            {%else%}
            <a href="{{spec.use_cases_url}}">
            <img src="/images/use_case_spec.png" alt="View BioSchemas {{ spec.spec_info.title }} Use Cases">
            </a>
            {%endif%}
          </td>
          <td class="spec_links">
            {% if spec.cross_walk_url == '' %}
            <a>
            <img src="/images/cross_walk.png" alt="View BioSchemas {{ spec.spec_info.title }} Cross Walk"  style="filter: grayscale(100%);">
            </a>
            {%else%}
            <a href="{{spec.cross_walk_url}}" target="_blank">
            <img src="/images/cross_walk.png" alt="View BioSchemas {{ spec.spec_info.title }} Cross Walk">
            </a>
            {%endif%}
          </td>
          <td class="spec_links">
            {% if spec.gh_tasks == '' %}
            <a>
            <img src="/images/specs_tasks.png" alt="BioSchemas {{ spec.spec_info.title }} Github Tasks or Issues" style="filter: grayscale(100%);">
            </a>
            {% else %}
            <a href="{{spec.gh_tasks}}" target="_blank">
            <img src="/images/specs_tasks.png" alt="BioSchemas {{ spec.spec_info.title }} Github Tasks or Issues">
            </a>
            {% endif %}
          </td>
          <td class="spec_links">
            {% if spec.spec_info.full_example == '' %}
            <a>
            <img src="/images/spec_examples.png" alt="View BioSchemas {{ spec.spec_info.title }} Examples" style="filter: grayscale(100%);">
            </a>
            {% else %}
            <a href="{{spec.spec_info.full_example}}" target="_blank">
            <img src="/images/spec_examples.png" alt="View BioSchemas {{ spec.spec_info.title }} Examples">
            </a>
            {% endif %}
          </td>
          <td class="spec_links">
            {% if spec.live_deploy == '' %}
            <a>
            <img src="/images/live_deploy.png" alt="View BioSchemas {{ spec.spec_info.title }} Examples" style="filter: grayscale(100%);">
            </a>
            {% else %}
            <a href="{{spec.live_deploy}}">
            <img src="/images/live_deploy.png" alt="View BioSchemas {{ spec.spec_info.title }} Examples">
            </a>
            {% endif %}
          </td>
      </tr>
      {% endfor %}
      </tbody>
  </table>
</div>


<h2>Types</h2>
<p>We have found it necessary to propose some additional types to the Schema.org vocabulary. 
    These are specified below and are expected to be pushed up to Schema.org once they have stabilised. 
    These types are used as the generic base for some of the profile specifications, such as protein.
    Again, working versions are published in the <a href="/drafts">drafts</a> page.</p>

<table class="bioschemas_spec_list" style="width: 100%; margin-left: auto; margin-right: auto; text-align: center;">
    <thead>
    <tr>
        <th>Name</th>
        <th style="text-align: center;">Group</th>
        <th style="text-align: center;">Task &amp; Issues</th>
    </tr>
    </thead>
    <tbody>
    {% assign type_specs = site.types | where: 'spec_type', 'Type'%}
    {% for spec in  type_specs%}
    <tr>
        <th><a href="/types/{{spec.name}}" title="{{spec.subtitle}}">{{ spec.name }}</a><br />(v{{spec.version}})<br />{{spec.dateModified}}</th>
        <td>
        {% assign group = site.groups | where:"identifier", spec.group | first %}
        <a href="{{group.url}}">{{group.name}}</a>
        </td>
        <td class="spec_links">
            {% if spec.gh_tasks == '' %}
              <a>
                <img src="/images/specs_tasks.png" alt="BioSchemas {{ spec.name }} Github Tasks or Issues" style="filter: grayscale(100%);">
              </a>
            {% else %}
              <a href="{{spec.gh_tasks}}">
                <img src="/images/specs_tasks.png" alt="BioSchemas {{ spec.name }} Github Tasks or Issues">
              </a>
            {% endif %}
        </td>
    </tr>
    {% endfor %}
    </tbody>
</table>
