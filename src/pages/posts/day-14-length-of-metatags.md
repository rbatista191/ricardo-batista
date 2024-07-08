---
layout: ../../layouts/post.astro
title: "Day 14: Getting the lengths of meta title and description right"
pubDate: 2024-06-27
description: "Day 14: Getting the lengths of meta title and description right"
author: "rbatista19"
excerpt: I am sharing every day a lesson I learned while building my last products. Today it will be about the lengths of meta title and description right.
image:
  src: /day14.png
  alt:
tags: ["technical seo", "metatags"]
---

_(This post was originally [shared on X](https://x.com/rbatista19/status/1806206455764148407))_

I am sharing every day a lesson I learned while building my last products.

Every time I produce a title and metadescription on my blog articles, it is a mess to keep getting them within the advisable limits: 50-70 characters for title, 110-160 for metadescription.

Even when I use @aiblogarticles to generate the article, the LLM often doesn’t stick to the advisable length.

I fixed this problem with a simple Python script. It uses OpenAI to understand the article context to produce the best sentence possible. And I [published it for everyone](https://gist.github.com/rbatista191/e3385845b4a506cc06c119fb59c691b2).

Tomorrow let’s talk about site speed!