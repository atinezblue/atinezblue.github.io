# atinezblue.github.io

Landing page and root-domain assets for Dat Vu's mobile apps and games.

Live at <https://atinezblue.github.io/>.

## What lives here

| Path | Served at | Purpose |
|---|---|---|
| `index.html` | https://atinezblue.github.io/ | Product showcase. Each entry carries its release status and links to its privacy policy and support page. |
| `app-ads.txt` | https://atinezblue.github.io/app-ads.txt | IAB authorized-seller declaration for AdMob (publisher `pub-7939235876248274`). Must stay at the domain root — AdMob's crawler ignores subdirectories. |
| `assets/*.png` | — | App icons, downscaled to 256px. |

Privacy policy and support pages themselves live in the separate
[`game`](https://github.com/atinezblue/game) repo, served under
https://atinezblue.github.io/game/.

## Adding a product

Copy an `<article class="product">` block in `index.html`, drop a 256px icon
into `assets/`, and set the status chip:

- `<span class="chip live">Available</span>` plus a real `<a class="store">` link
- `<span class="chip soon">Coming soon</span>` plus `<span class="store pending">`

## Store listing requirement

AdMob resolves `app-ads.txt` from the developer website on the store listing, so
the **Website** field in Google Play Console and the **Marketing URL** field in
App Store Connect must both point at `https://atinezblue.github.io/`. The
crawler keeps only the hostname and fetches `/app-ads.txt` from the root.
