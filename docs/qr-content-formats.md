# QR content formats

What to encode in each template's QR. Paste these into any generator — or create them at [qrlytix.com](https://qrlytix.com/qr-code-generator) with scan tracking.

> Replace everything in `<angle brackets>`. Keep the rest exactly as written.

## UPI payment — *Payment Standee*

```
upi://pay?pa=<your-upi-id>&pn=<Store%20Name>&cu=INR
```

- `pa` — your UPI ID, e.g. `store@okaxis`
- `pn` — payee name, spaces as `%20`
- Optional: `&am=<amount>` for a fixed amount, `&tn=<note>` for a note

Works with GPay, PhonePe, Paytm, BHIM and every UPI app. Leave out `am` on a counter standee so customers enter the amount.

## Wi‑Fi — *Wi‑Fi Card*

```
WIFI:T:WPA;S:<network name>;P:<password>;H:false;;
```

- `T` — `WPA` (covers WPA2/WPA3), `WEP`, or `nopass` for open networks
- `H:true` if the network is hidden
- Escape `\ ; , : "` with a backslash: `P:cafe\;2026`

iPhone (iOS 11+) and Android join with one tap from the camera.

## Contact card — *Business Card*

```
BEGIN:VCARD
VERSION:3.0
N:<Last>;<First>
FN:<First Last>
ORG:<Company>
TITLE:<Job title>
TEL;TYPE=CELL:<+91XXXXXXXXXX>
EMAIL:<you@company.com>
URL:<https://company.com>
ADR;TYPE=WORK:;;<Street>;<City>;;<PIN>;<Country>
END:VCARD
```

Keep it short — every extra field makes the code denser and harder to scan on a small card. If you need more, link to a contact page instead.

## Google review — *Review Card*

```
https://search.google.com/local/writereview?placeid=<PLACE_ID>
```

Find your Place ID with Google's [Place ID Finder](https://developers.google.com/maps/documentation/places/web-service/place-id). Or copy the **Ask for reviews** link from your Google Business Profile — it's shorter.

## App download — *App Download Card*

One QR can't open both stores on its own. Use a smart link that detects the phone and redirects:

- iPhone → `https://apps.apple.com/app/id<APP_ID>`
- Android → `https://play.google.com/store/apps/details?id=<package.name>`

QRlytix and most dynamic-QR tools offer this as one link.

## WhatsApp chat

```
https://wa.me/<countrycode><number>?text=<Hi%2C%20I%20saw%20your%20sign>
```

Number without `+`, spaces or dashes: `919XXXXXXXXX`.

## Instagram — *Instagram Story*

```
https://instagram.com/<username>
```

## Email / SMS / Call

```
mailto:<you@company.com>?subject=<Hello>
SMSTO:<+91XXXXXXXXXX>:<message>
tel:<+91XXXXXXXXXX>
```

## Location

```
https://maps.google.com/?q=<lat>,<lng>
geo:<lat>,<lng>
```

`geo:` opens the default maps app; the Google Maps link works everywhere.

## Menu, property, RSVP, badge, product label

Use a plain URL. For anything printed in bulk, a **dynamic QR** is safer: the code points to a short link you can change later — new menu prices, a sold property, a moved RSVP form — without reprinting.

```
https://<your-short-link>
```

## Static vs dynamic

| | Static | Dynamic |
|---|---|---|
| Content fixed forever | Yes | No — editable after printing |
| Scan analytics | No | Yes |
| Code density | Grows with content | Always short |
| Best for | Wi‑Fi, vCard, UPI | Menus, signs, campaigns |

---

Generate, edit and track your codes at **[qrlytix.com](https://qrlytix.com/qr-code-generator)**.
