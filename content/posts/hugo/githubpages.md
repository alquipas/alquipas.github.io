---
title: "Creating My Own Static Website III"
date: 2020-12-19T13:49:00Z
draft: false
---
## GitHub Pages
[GitHub Pages](https://pages.github.com/) is a service that allows us to host our static website [directly from our repository](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/creating-a-github-pages-site) on GitHub for free. They even let you expel a certificate for your website and configure a [custom domain name](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site).

So I planned to use GitHub Pages as a hosting service for my website, Cloudflare for managing my DNS zone and as a reverse proxy to improve the performance of my content delivery, and both of them to have free certificates.

As I'm using [hugo](https://gohugo.io/) for building my static website I can't publish my whole repository as a website, because there're a lot of files that the website doesn't need. At first, I thought of some complicated way of CI/CD with [GitHub Actions](https://github.com/features/actions), a great new service that I wanted to try, but GitHub Pages allows you to configure a [publishing source](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site), so I just needed to configure on my config.toml the right directory.

> publishDir = "docs"

Finally, this is how I update my website, I create a new Markdown file, with the content that I want, test it locally with the following command and when I am happy with the result I build the static content and push it to the repository. Github Pages and Cloudflare are responsible for everything else.

> HUGO_ENV=production hugo server # Command to test the new content locally

> HUGO_ENV=production hugo --minify # Command to build the static content

