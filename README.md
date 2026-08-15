# biddlesystems.com

Landing page for Biddle Systems LLC. Static, single file, no build step.

- `index.html` — the whole site. Self-contained: no external fonts, scripts, or images.
- `CNAME` — tells GitHub Pages to serve this at `biddlesystems.com`. Don't delete it.

## Deploying

Push to `main`. GitHub Pages rebuilds automatically, usually within a minute.

```
git add -A
git commit -m "your message"
git push
```

## DNS

The apex domain points at GitHub's Pages IPs, with `www` as a CNAME. Records live in
Hostinger's hPanel under Domains → DNS / Nameservers.
