# MangoMelon Studio 🍈🥭

[**www.mangomelon.studio**](https://www.mangomelon.studio)

MangoMelon Studio is a small independent studio building **gentle, playful
software for families**. We care about apps that feel warm, useful, and
trustworthy — not apps that push endless engagement.

Across our products the goal is the same: calm design, clear utility,
family-friendly privacy, and a little bit of joy.

---

## Our products

### 🐰 Bumochi — gentle time management for kids 6+

A bunny pet companion that helps kids build daily routines through quests,
healthy breaks, and a weekly review parents can actually use. Local-first,
no ads, no engagement traps. The name is a Chinese pun on *不磨叽* — "no dawdling."

→ [mangomelon.studio/bumochi](https://www.mangomelon.studio/bumochi/)

### 🦆 SquishyDuck — soft stress relief

Squeeze, breathe, and unwind with a little duck companion. SquishyDuck started
the studio's product journey — tactile, playful interactions designed to make
quick calming moments feel lighter.

→ [Download on the App Store](https://apps.apple.com/us/app/squishy-duck/id6751784205)
→ [mangomelon.studio/squishyduck](https://www.mangomelon.studio/squishyduck/)

---

## What we believe

- **Privacy by default.** No third-party ad SDKs, no behavioral tracking, no
  data brokers. Where possible, data stays on the device.
- **Calm, not addictive.** No streaks-as-pressure, no casino-style reward
  loops, no notifications nagging you to come back.
- **Family-friendly.** Designed so parents can hand a phone to a kid without
  worrying about what's on the other side of a tap.
- **Small and patient.** We'd rather ship something gentle and slow than
  something loud and extractive.

---

## Get in touch

- General & press: [support@mangomelon.studio](mailto:support@mangomelon.studio)
- Bumochi support: [support@mangomelon.studio](mailto:support@mangomelon.studio?subject=Bumochi)
- SquishyDuck support: [support@mangomelon.app](mailto:support@mangomelon.app?subject=SquishyDuck)

---

## About this repository

This repo holds the static site for **www.mangomelon.studio**, served via
GitHub Pages. No build step — just plain HTML, Tailwind via CDN, and a small
shared design-token stylesheet ([`mm.css`](./mm.css)) derived from the
MangoMelon Studio design system (warm Morandi palette + Fraunces / Nunito /
Caveat Brush).

```text
index.html                       # Studio homepage
contact/index.html               # Contact page
bumochi/index.html               # Bumochi product page
bumochi/privacy/index.html       # Bumochi privacy policy
squishyduck/index.html           # SquishyDuck product page
squishyduck/privacy/index.html   # SquishyDuck privacy policy
mm.css                           # Shared design tokens
CNAME                            # GitHub Pages custom domain
```

To preview locally:

```bash
python3 -m http.server 4173
# open http://localhost:4173
```

---

© MangoMelon Studio LLC. Gentle family software, built with care.
