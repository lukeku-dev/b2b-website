# TP Global – B2B Product Catalog Website

A multi-page static website for **TP Global**, an industrial packaging distributor based in the US. Built entirely with vanilla HTML, CSS, and JavaScript — no frameworks, no build tools, no dependencies.

## Overview

This site serves as a B2B product catalog, allowing wholesale buyers to browse product specifications and submit price inquiries. It covers 8 product categories across 20 pages, with consistent design and navigation throughout.

**Live site:** *(add URL when deployed)*

## Features

- **20 product pages** with detailed spec sheets in a consistent badge/pill UI
- **Tab-based product navigation** with URL parameter support (`?tab=xxx`)
- **Price inquiry form** on every product page with product pre-selection
- **Responsive navigation** with desktop dropdowns and mobile menu
- **No external dependencies** — pure HTML/CSS/JS, loads instantly

## Product Categories

| Category | Page |
|---|---|
| Tapes (OPP, PVC, Flagging, Labels) | `tapes.html` |
| Stretch Film (Blown, Cast, Machine Grade, Banding) | `stretch-film.html` |
| Strapping Products (PET, PP, Steel) | `strapping-products.html` |
| Bags & Mailers | `bags-mailers.html` |
| Cardboard Boxes (Single Wall, Double Wall) | `cardboard-box.html` |
| Protective Materials | `protective-materials.html` |
| Warehouse Supplies | `warehouse-supplies.html` |
| Janitorial & Cleaning | `janitorial-cleaning.html` |

## Project Structure

```
b2b-website/
├── index.html                  # Homepage with product grid
├── tapes.html
├── stretch-film.html
├── strapping-products.html
├── cardboard-box.html
├── bags-mailers.html
├── protective-materials.html
├── warehouse-supplies.html
├── janitorial-cleaning.html
├── [other category pages]
└── *.webp                      # Product images
```

## Design System

All pages share a consistent design language:

- **Colors:** Navy `#1c3557` (primary), Red `#c8391a` (accent)
- **Fonts:** Montserrat (headings), Inter (body)
- **Spec display:** Badge/pill style — `.spec-row` > `.spec-row-label` + `.tag-group` > `.spec-tag`
- **Layout:** Max-width 1200px centered, 2-column product layout (image + info)

## Maintenance Notes

**To add a new product tab:**
1. Add a `<button class="tab-btn" onclick="switchTab('id')">` in the tab bar
2. Add a `<div class="tab-content" id="tab-id">` with the product section
3. Add the tab link to the nav dropdown in **all 20 pages**
4. Add the option to the inquiry form `<select>` in that page

**To update specs:** Edit the `.spec-tag` elements inside the relevant `tab-content` div.

**To add a new page:** Copy the closest existing page as a template, update the nav `active` class, breadcrumb, page title, and content.

## Tech Stack

- **HTML5 / CSS3 / Vanilla JS** — zero build step, open any file in a browser
- **Google Fonts** — Inter + Montserrat via CDN
- **Git** — version controlled on GitHub
