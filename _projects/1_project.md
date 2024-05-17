---
layout: distill
title: sentence qualia structure
description: Modeling phenomenal similarity of global states of consciousness leveraging LLMs
img: assets/img/12.jpg
importance: 1
category: work
related_publications: true
tags: qualia
giscus_comments: false
date: 2024-05-17
featured: true

authors:
  - name: Zoe Youngzie Lee
    affiliations:
      name: UCLA
  - name: Norie Kawamura
    affiliations:
      name: ATR   
  - name: Naotsugu Tsuchiya
    affiliations:
      name: Monash University
  - name: Martin Monti
    affiliations:
      name: UCLA


# bibliography: 2018-12-22-distill.bib

# Optionally, you can add a table of contents to your post.
# NOTES:
#   - make sure that TOC names match the actual section names
#     for hyperlinks within the post to work correctly.
#   - we may want to automate TOC generation in the future using
#     jekyll-toc plugin (https://github.com/toshimaru/jekyll-toc).
toc:
  - name: Background
    # if a section has subsections, you can add them as follows:
    # subsections:
    #   - name: Example Child Subsection 1
    #   - name: Example Child Subsection 2
  - name: Methods
  - name: Interactive Plots


# Below is an example of injecting additional post-specific styles.
# If you use this post as a template, delete this _styles block.
_styles: >
  .fake-img {
    background: #bbb;
    border: 1px solid rgba(0, 0, 0, 0.1);
    box-shadow: 0 0px 4px rgba(0, 0, 0, 0.1);
    margin-bottom: 12px;
  }
  .fake-img p {
    font-family: monospace;
    color: white;
    text-align: left;
    margin: 12px 0;
    text-align: center;
    font-size: 16px;
  }
---

## Background

Here we leverage LLMs to derive the similarity structure between phenomenal experiences described in short sentences.
some background will be added here
Citations are then used in the article body with the `<d-cite>` tag.

---

## Methods

The key attribute is a reference to the id provided in the bibliography.
The key attribute can take multiple ids, separated by commas.

The citation is presented inline like this: <d-cite key="gregor2015draw"></d-cite> (a number that displays more information on hover).

Add Details boxes (collapsible boxes which hide additional information from the user) for detailed methods. They can be added with the `details` liquid tag:

{% details Click here to know more %}
Additional details, where math $$ 2x - 1 $$ and `code` is rendered correctly.
{% enddetails %}


---

## Interactive Plots

You can add interative plots using plotly + iframes :framed_picture:

<div class="l-page">
  <iframe src="{{ '/assets/plotly/demo.html' | relative_url }}" frameborder='0' scrolling='no' height="500px" width="100%" style="border: 1px dashed grey;"></iframe>
</div>
