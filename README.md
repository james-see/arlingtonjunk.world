# Arlington Junk — arlingtonjunk.world

Single-file landing page for an Arlington, VA junk removal business.
Deployed via GitHub Pages (same setup as the guitar lessons site).

## Preview

```sh
open index.html
# or
python3 -m http.server 8000
```

## Files

- `index.html` — the whole site (Tailwind via CDN, dark mode, SEO + LocalBusiness/FAQ schema)
- `CNAME` — custom domain for GitHub Pages (`arlingtonjunk.world`)

## Still placeholder (swap with real content)

- Testimonial quotes (marked "Sample quote" in `index.html`)
- `$99` starting price — confirm your minimum before launch
- Service area: NoVA (Arlington/Fairfax/Loudoun + Alexandria), DC, Potomac MD — matches listings

## Domains

- Primary: `arlingtonjunk.world` (CNAME + canonical URL)
- Secondary: `arlingtonjunkremoval.world` — forward to primary in Namecheap (see below)

## Launch checklist (Namecheap + GitHub)

1. Push this repo, then enable Pages: repo Settings → Pages → Deploy from branch `main`, folder `/ (root)`. Add custom domain `arlingtonjunk.world` and tick Enforce HTTPS once DNS resolves.
2. Namecheap → Domain List → `arlingtonjunk.world` → Advanced DNS:
   - `A @ → 185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME www → <github-username>.github.io.` (trailing dot required by Namecheap)
3. Namecheap → `arlingtonjunkremoval.world` → Advanced DNS: delete default records, add `URL Redirect @ → https://arlingtonjunk.world` (permanent 301) and `CNAME www → https://arlingtonjunk.world` (or same redirect host).
4. Wait for DNS (minutes–hours), verify `https://arlingtonjunk.world` loads, then tick Enforce HTTPS in Pages settings.
