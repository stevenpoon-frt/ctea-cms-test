# cms-content

Git-backed **news / media** for the CTEA CMS pilot. This repository should be **public** so the **cms-test** site can fetch Markdown (and media via jsDelivr) at runtime with no token and no redeploy on every post.

Edited by [Sveltia CMS](https://sveltiacms.app/) from cms-test (`/admin/`). This repo has **no website** — only content.

## Layout

```text
news/          Markdown posts (frontmatter + body)
media/         Images and files referenced by posts
```

## Frontmatter

```yaml
---
title: Example
date: 2026-06-08
category: 協會消息   # 賽事公告 | 協會消息 | 教育推廣 | 國際交流
excerpt: Short summary
featured: true
---

Markdown body…
```

## Who commits here

- Editors via Sveltia (GitHub OAuth / token) → commits land on this repo  
- Developers may edit Markdown in Git as usual  

After a push to the default branch, refresh the cms-test site — it reads this public repo live via the GitHub Contents API.
