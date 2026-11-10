# biddlesystems.com

Live site for Biddle Systems LLC, served by GitHub Pages from `main` with the custom domain in `CNAME`.

## Where the site comes from

The marketing pages are BUILT, not edited here. The source is the cinematic preview repo
(`C:\ClaudeCode\biddlesystems-cinematic-preview`, github.com/mwb05/biddlesystems-cinematic-preview),
which the Site Editor edits and which is served at https://mwb05.github.io/biddlesystems-cinematic-preview/.
To publish the preview here:

```
cd C:\ClaudeCode\biddlesystems-cinematic-preview
node build.mjs --prod --out=C:\Sites\biddlesystems
cd C:\Sites\biddlesystems
git add <the changed pages and assets>
git commit -m "Publish preview <commit>"
git push origin main
```

`--prod` drops the preview-only noindex tag and "Preview" chip; everything else is identical.
Generated: index.html, about/ accessibility/ automation/ contact/ courses/ privacy/ process/ proof/
savings/ services/ sms-terms/ terms/ tool/, styles.css theme.css site.css heroes.css script.js fx.js
calc.js favicon.svg fonts/ .nojekyll.

## Hand-kept files (not generated, don't delete)

- `CNAME` - tells GitHub Pages to serve this at biddlesystems.com.
- `demos/family-law-intake/` - public, noindexed prospect demo.
- `f/` and `404.html` - the hosted-forms renderer. GitHub Pages serves 404.html for unknown paths,
  and /f/<slug> renders that form from the forms API.
- `sms.html` - SMS program opt-in page for the toll-free number +1 (855) 382-7849 (Twilio
  toll-free verification). `sms-optin-proof.png` is a screenshot of it.
- `thanks.html` - the contact form (Web3Forms) redirects here after a send.
- `privacy.html`, `sms-terms.html` - redirects to /privacy/ and /sms-terms/, kept because the old
  URLs are on file with Twilio.

## DNS

The apex domain points at GitHub's Pages IPs, with `www` as a CNAME. Records live in
Hostinger's hPanel under Domains -> DNS / Nameservers.