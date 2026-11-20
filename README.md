# The alt text gap, 2026

A measurement of alt text on e-commerce homepages, published 17 November 2026 and refreshed since.

**48 homepages · 2,649 images · 970 without a text alternative (36.6%)**

The finding worth your time: **841 of those 970 images carried an empty `alt=""` rather than a missing
attribute.** Empty alt passes validators that check for the attribute's presence, and screen readers skip the
image silently — so a page can "have alt text" and still be blank for anyone not looking at it.

Also in this sample: 225 images shared their alt text with two or more other images on the same page (the same
sentence on six colourways), 22 used filenames, 39 said "Image" or "Image unavailable", 98 were over 125
characters, 69 repeated a word three or more times, and 1,317 had nothing wrong at all.

## The data

[`alt-text-gap-2026.csv`](alt-text-gap-2026.csv) — one row per homepage:

| column | meaning |
| --- | --- |
| `domain` | the store |
| `homepage` | URL fetched |
| `images` | `<img>` elements counted (tracking pixels, inline SVG and empty `src` excluded) |
| `without_text_alternative` | alt attribute absent **or** empty |
| `missing_attribute` | no `alt` attribute at all |
| `empty_attribute` | `alt=""` present |
| `share_without` | share of images without a text alternative |

## Method and limits

Plain HTTP fetch of one page per site, parsed for `<img>`; no JavaScript rendering; one snapshot in time. Sites
that refused the request (bot protection) or that returned too little server-rendered HTML were excluded rather
than counted as failures. This is a description of the sample, not a conformance audit.

## Who measured

[AltTextFix](https://alttextfix.com/reports/alt-text-gap-2026) (Pixelforge LLC) — we write alt text for
catalogues, so treat this as vendor data; the method and every row are here so you can check or refute it.
Corrections are published. The tool used is open source: [beta-alttext-cli](https://github.com/ascelio-co/beta-alttext-cli).
