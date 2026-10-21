# Spring Engineering Website

Plain HTML/CSS/JS one-page site for www.spring.net.au. No build step. GitHub Pages deploys the repo root on every push to `main`.

## Files

- `index.html`: page content, CSS and JS
- `images/`: the 21 photos (.webp)

## Things to know

- **Enquiry form:** it doesn't post to a server. When someone submits it, their own email app opens with a pre-filled email to `hello@spring.net.au`. To capture enquiries directly instead (e.g. Formspree, Netlify Forms, HubSpot or your own endpoint), swap the `submit` handler at the bottom of the `<script>` block for a real form `action`. The field names are `name`, `phone`, `type`, `timing`, `site` and `message`.
- **Font:** Inter is loaded from Google Fonts. If that's blocked, the page falls back to the system font.
- **Animations:** sections fade in on scroll. Users with "reduce motion" switched on get no animation.
- **Responsive:** tested at 375 px (phone), 1024 px and desktop widths. There's no horizontal scrolling.
- **Accessibility:** every photo has alt text and the mobile menu has ARIA attributes.
- **SEO:** title, meta description and Open Graph tags are set in `<head>`. Consider adding an `og:image` (e.g. `images/hero.webp` as an absolute URL), a favicon and Google Analytics/Tag Manager if you use them.

## Content to confirm with the client before launch

The page doesn't include any invented prices, reviews or statistics. These statements should still be checked with the business:

- "Fixed-fee proposals" and "Free initial project review"
- "Approval-ready documentation" (council / certifier)
- "Projects across Australia"
- Bushfire (BAL) deck design considerations
- The gallery is headed **"Example project types"** because the photos are stock images, not Spring projects. Swap them for real project photos when available.
- There's no ABN, phone number, address or social links yet. Add them to the footer and contact section if wanted.

## Photos

All photos are from Unsplash, under the [Unsplash License](https://unsplash.com/license): free for commercial use, no attribution required. Original sources:

| File | Source |
|---|---|
| hero.webp | https://images.unsplash.com/photo-1600585154340-be6161a56a0c |
| framing.webp | https://images.unsplash.com/photo-1589939705384-5185137a7f0f |
| drawings.webp | https://images.unsplash.com/photo-1600563438938-a9a27216b4f5 |
| cladding.webp | https://images.unsplash.com/photo-1600573472592-401b489a3cdc |
| prefab.webp | https://images.unsplash.com/photo-1600047509807-ba8f99d2cdde |
| studio.webp | https://images.unsplash.com/photo-1591825729269-caeb344f6df2 |
| deck.webp | https://images.unsplash.com/photo-1595877244574-e90ce41ce089 |
| site.webp | https://images.unsplash.com/photo-1541888946425-d81bb19240f5 |
| docs.webp | https://images.unsplash.com/photo-1503387762-592deb58ef4e |
| band.webp | https://images.unsplash.com/photo-1542718610-a1d656d1884c |
| g_pool.webp | https://images.unsplash.com/photo-1564013799919-ab600027ffc6 |
| g_cabin.webp | https://images.unsplash.com/photo-1587061949409-02df41d5e562 |
| g_wrap.webp | https://images.unsplash.com/photo-1558036117-15d82a90b9b1 |
| g_modern.webp | https://images.unsplash.com/photo-1523217582562-09d0def993a6 |
| g_interior.webp | https://images.unsplash.com/photo-1618221195710-dd6b41faaea6 |
| g_red.webp | https://images.unsplash.com/photo-1518780664697-55e3ad937233 |
| a_home.webp | https://images.unsplash.com/photo-1480074568708-e7b720bb3f09 |
| a_builder.webp | https://images.unsplash.com/photo-1504307651254-35680f356dfd |
| a_arch.webp | https://images.unsplash.com/photo-1600596542815-ffad4c1539a9 |
| materials.webp | https://images.unsplash.com/photo-1560185007-cde436f6a4d0 |
| contact.webp | https://images.unsplash.com/photo-1510798831971-661eb04b3739 |

To replace a photo in the `editable/` version, overwrite the file in `images/` with the same name, or change the `src` in `index.html`. Keep the image orientation roughly the same, because the layout crops with `object-fit: cover`.
