---
redirect_from:
  - "/guide/05-advanced"
title: 'How-to and advanced topics'
prev_page:
  url: /guide/04_faq.html
  title: 'FAQ'
next_page:
  url: /features/features.html
  title: 'Features and customization'
comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"
---
This page contains more advanced and complete information about the
[`jupyter-book` repository](https://github.com/jupyter/jupyter-book). See the sections below.

## Enable Google Analytics

If you have a Google Account, you can use Google Analytics to collect some 
information on the traffic to your Jupyter Book. With this tool, you can find 
out how many people are using your site, where they come from and how they 
access it, wether they are using the Desktop or the mobile version etc. 

To add Google Analytics to your Jupyter Book, navigate to 
[Google Analytics](https://analytics.google.com/analytics/web/), create a new 
Google Analytics account and add the url of your Jupyter Book to a new 
*property*. Once you have set everything up, your Google Analytics property 
will have a so-called Tracking-ID, that typically starts with the letters UA. 
All that you need to do is to copy this ID and paste it into your 
configuration file:

```yaml
google_analytics:
  mytrackingcode: UA-XXXXXXXXX-X
```

## Retain custom YAML front-matter in your files

Jupyter book will check your files for YAML front-matter and will **append**
any newly-generated YAML to the built files for the page. This means you
can provide your own custom YAML to files (which may be useful if you'd like
to modify this site's HTML).

Be careful not to add YAML with the same key names as the auto-generated YAML, as
this will create duplicated keys in your page's front-matter.


## Deploying a JupyterHub

If you wish, you may deploy a JupyterHub alongside your textbook. This way, for pages that are built from
Jupyter Notebooks, students can click the "interact" links
at the top of each page and be taken to a live Jupyter Notebook running on your JupyterHub.

The easiest way to set up a JupyterHub is to follow [The Littlest JupyterHub guide](https://the-littlest-jupyterhub.readthedocs.io/en/latest/index.html).
This is a straightforward deployment of JupyterHub on a single VM, and is suitable for
courses / workshops of less than 50-60 students.

Once you have your JupyterHub set up, you can use the [nbgitpuller](https://github.com/data-8/nbgitpuller)
package to send links to course material to your students, or use the interact links that Textbooks for Jupyter
automatically inserts into your course material.
