---
title: "Creating My Own Static Website II"
date: 2020-12-18T21:11:00Z
draft: false
---
## Cloudflare
Talking with a former colleague but great friend, [Dani](https://www.instagram.com/dmglife.es/), about hardening security on websites, lower the access time and improve reliability he mentioned [Cloudflare](https://www.cloudflare.com) as a good service to obtain all that and at a low price (free).

I was skeptical at first because "there's no such thing as free lunch", but just when creating an account and looking at all the features that they give you for free changed my mind. I was able to configure a certificate for my domain for free, improve the delivery of my content with their cache and auto minifying to reduce the size of the source code, force to use HTTPS, enforce HSTS, increase the minimum TLS version to 1.2, enable TLS 1.3, configure automatic rewrites to HTTPS, without me having to configure anything in my nginx configuration. I even stopped my nginx and as my website is all static content Cloudflare's cache served my website anyway.

> TL;DR so many cool features and there's even more if you pay for other tiers.

So I knew that I wanted to use Cloudflare as proxy for my website.

This is a great service, because  you can for free improve your security and performance just by puting a reverse proxy.

