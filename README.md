# Community portal

This is the repository of Community portal. The current online version of this portal can be found at https://community.torproject.org or [Community Onion Service](http://xmrhfasfg5suueegrnc4gsgyi2tyclcy5oz7f5drnrodmdtob6t2ioyd.onion/).

To clone the code use either of 

```git clone https://gitlab.torproject.org/tpo/web/community.git```

```torify git clone http://eweiibe6tdjsdprb4px6rqrzzcsi22m4koia44kc5pcjr7nec2rlxyad.onion/tpo/web/community.git/``` 

or browse it [online](https://gitlab.torproject.org/tpo/web/community).

## How to report bugs or feedback 

First, check if the bug is already known. You can search and read all the issues at https://gitlab.torproject.org/. To create a new issue, please [request a new account](https://gitlab.onionize.space/) to access Tor Project's GitLab instance and [find the right repository](https://gitlab.torproject.org/tpo) to report your issue. Issues related to our websites should be filed under the [Web issue tracker](https://gitlab.torproject.org/groups/tpo/web/-/issues).

## What is Lektor

[Lektor](https://www.getlektor.com/) is a framework to generate and serve websites from Markdown files.

Its code can be found at [GitHub](https://github.com/lektor/lektor).

## How to contribute

### (Easy) Edit this page button

You can click ```Edit this page``` and submit your content changes in a [Pull Request in GitLab](https://gitlab.torproject.org/tpo/web/community/-/merge_requests/).

### (Advanced) Compiling a local version of the website

See this guide on our wiki: https://gitlab.torproject.org/tpo/web/team/-/wikis/documentation/Compiling-a-local-version-of-the-website

### Translations

To help us to translate, please join the [Tor Project team](https://hosted.weblate.org/projects/tor/) on Weblate.

### Getting help

If you want to contribute to the Community portal, we will be happy to help you. Join us at #tor-www in [irc.oftc.net](https://www.oftc.net).

### The community-generator plugin

This lektor site uses a special plugin called `community-generator`, you can find it in the `packages` directory. This plugin generates a special set of lektor contents files used for a js-free filtering system on the training resources page.

You shouldn't need to do anything or know anything about this plugin in order to use it. If you want to develop on this plugin, see the plugin's [README](packages/community-generator/README.md).

#### Adding training guides for training resources

Each training resource can optionally have a training guide. You can create a training guide for a particular resource by creating a new lektor contents file with the path `content/training/resources/<resource name>-guide/contents.lr`. So to create a guide for a resource called `all-about-tor`, you would create `content/training/resources/all-about-tor-guide/contents.lr`. Here's an example contents file for a training guide:

```
_model: resource
---
title: All About Tor Training Guide
---
author: Tor Project
---
cover:
---
background: white
---
image: /static/images/onion.png
---
body: body test goes here!
---
external_sources:
https://www.acsac.org/2011/program/keynotes/syverson.pdf
https://matt.traudt.xyz/posts/2021-02-22-tor-spelling/
---
objectives:
Understand the privacy advantages of the Tor network.
Understand the breadth of the Tor ecosystem of tools.
Identify properties important in privacy-preserving technologies.
---
topics:
foo
bar
baz
---
sample_slides:

#### sample_slide ####
language: English
----
view_link: link to view the training guide
----
pdf_link: link to the pdf guide
----
odp_link: link to the odp guide
----

#### sample_slide ####
language: Español
----
view_link: link to view the training guide
----
pdf_link: link to the pdf guide
----
odp_link: link to the odp guide
```
