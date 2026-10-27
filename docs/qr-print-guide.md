# QR print guide

A short checklist for QR codes that scan the first time. From the team at [QRlytix](https://qrlytix.com/?ref=github-guide).

## Size

| Scan distance | Minimum QR size |
|---|---|
| Hand-held (business card, label) | 2 × 2 cm |
| Table / counter (≈ 30 cm) | 3 × 3 cm |
| Wall poster (≈ 1 m) | 10 × 10 cm |
| Sign / window (≈ 3 m) | 30 × 30 cm |

Rule of thumb: **QR width ≈ scan distance ÷ 10.**

## Contrast

- Dark modules on a light background. Inverted (light on dark) codes fail on many phone cameras.
- Contrast ratio of at least 4:1 between modules and background.
- Avoid printing over photos, gradients or textures.

## Quiet zone

Leave an empty margin of **4 modules** around the code (roughly 10% of the code's width). Every template in this repo keeps it — don't crop it when you swap in your own QR.

## Content

- **Shorter URL = simpler code = easier scan.** Use a dynamic/short link for long URLs.
- Add a clear call to action next to the code: *Scan to pay*, *Scan for menu*, *Scan to join Wi‑Fi*.
- Dynamic QR codes let you change the destination after printing — useful for menus and price lists.

## Wi‑Fi QR format

```
WIFI:T:WPA;S:<network name>;P:<password>;;
```

Use `T:nopass` for open networks. Escape `; , : \` with a backslash.

## Before you print 500 copies

- [ ] Print one proof at final size
- [ ] Scan with an iPhone and an Android phone
- [ ] Scan in the real lighting (restaurant, shop window, outdoors)
- [ ] Check the link opens the right page on mobile data
- [ ] Use matte paper or lamination to avoid glare

## Material

Matte or uncoated stock scans best. Glossy lamination can reflect light directly into the camera — test it under the actual lights.

---

Make and track your codes at **[qrlytix.com](https://qrlytix.com/?ref=github-guide)**.
