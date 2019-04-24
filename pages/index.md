---
permalink: /
redirect_from:
- projects/
- review/
- examples/
- about/
layout: default
---
<div id="landing" itemscope itemtype="http://schema.org/Organization">
   <meta itemprop="logo" content="{{ site.baseurl }}/{{ site.logo }}"/>
   <meta itemprop="url" content="{{ site.baseurl }}"/>
   <meta itemprop="email" content="{{ site.email }}"/>
   <meta itemprop="name" content="{{ site.name }} Community"/>
    
    <div class="container-flow">
    <div class="row">
    <div class="col-md-8">
    <h1>What is {{ site.name }}?</h1>
    <p>{{ site.name }} is a sibling of <a href="http://www.bioschemas.org" target="_blank">BioSchemas</a> 
       to support <a href="https://schema.org" target="_blank">schema.org</a> to provide data interoperability 
       for open science. The specifications here are related to technology, high performance computing,
       infrastructure and research computing. Users are encouraged to use this markup to provide
       structured understanding to content that drives programmatic discovery.</p>
    <p>The main outcome of Bioschemas is a collection of specifications that provide guidelines to facilitate a more consistent
       adoption of schema.org markup within the life sciences.</p>
    <p>Bioschemas started as a community effort in November 2015. It operates as an open community initiative with more than
    <a href="/people/">200 people</a> from a wide variety of institutions. You are welcome to
    <a href="https://www.github.com/openschemas/">join the community on GitHub</a>.</p>
    <h2>Schema.org</h2>
    <p>Schema.org provides a way for us to add semantic markup to web pages. It describes ‘types’ of information, which then have
       ‘properties’. For example, ‘Event’ is a type that has properties like ‘startDate’, ‘endDate’ and ‘description’. If types
       or properties needed in the life sciences are missing, then Bioschemas proposes their adoption by Schema.org.</p>
    <p>Schema.org is a community effort supported by the main search engines, and is already widely implemented across the web.</p>
    <h2>OpenSchemas for generic types</h2>
    <p>Schema.org defines common generic types like events and datasets which can be used in many  disciplines. Openschemas is   
       working on specifications to improve the description of generic types in open sciences, and specifically those that 
       might not fit cleanly into the category of "iife sciences."
       The dataset markup properties that Openschemas specifies as mandatory will also make them <a href="/software/index.html#googleDatasetSearch">findable by Google's Dataset Search.</a></p>
    </div>
    <div class="col-md-4 right-column">
    <section>            
    <a class="twitter-timeline" data-height="450" data-theme="light" data-link-color="#2BB673" href="https://twitter.com/{{ site.twitter }}?ref_src=twsrc%5Etfw">Tweets by {{ site.twitter }}</a>
    <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
    </section>
    </div>
    </div>
    </div>
</div>
