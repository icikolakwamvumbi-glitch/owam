# Velora Motors — Luxury & Performance Automotive Platform

## Student Details
* **Student Name:** Mvumbi Owam
* **Student ID:** ST10526553
* **Module Code:** WEDE5020 (Web Development)
* **Institution:** IIE Rosebank International

---

## Project Overview
Velora Motors is a responsive, multi-page digital showroom for high-performance and luxury vehicles. Automotive enthusiasts, collectors and prospective buyers can explore vehicle details, learn about brand heritage, investigate ownership and financing options, and request private viewings.

---

## File & Folder Structure

```text
Owam-Website/
├── css/
│   └── style.css
├── images/
│   ├── ferrari-296-gtb-800.jpg / -1600.jpg
│   ├── lamborghini-huracan-800.jpg / -1600.jpg
│   ├── rolls-royce-ghost-800.jpg / -1600.jpg
│   ├── bentley-bentayga-800.jpg / -1600.jpg
│   ├── range-rover-autobiography-800.jpg / -1600.jpg
│   ├── aston-martin-db12-volante-800.jpg / -1600.jpg
│   └── jaguar-e-type-800.jpg / -1600.jpg
├── screenshots/
│   ├── desktop.png
│   ├── tablet.png
│   └── mobile.png
├── index.html
├── showroom.html
├── about.html
├── heritage.html
├── ownership.html
├── contact.html
└── README.md
```

---

## Changelog

### Part 2 feedback corrections (made in Part 3)

| # | Lecturer feedback | What was wrong | Change made | Files affected |
|---|---|---|---|---|
| 1 | Stylesheet path problem: HTML requested `css/style.css` but the submission had a single file literally named `css` with no extension. | The stylesheet was saved as a file called `css`, so the browser could not find `css/style.css` and the site loaded unstyled. | Created a real `css/` folder containing `style.css`. Every page links to `css/style.css`. | `css/style.css`, all `.html` files |
| 2 | Every vehicle image path was broken (e.g. `ferrari-296-gtb.jpg` was really `ferrari-296-gtb.jpg.jpg`). | All seven images had a double `.jpg.jpg` extension (and `bentley-bentayge` was misspelt). | Renamed every image with a single, correct extension and fixed the Bentayga spelling. HTML paths now match the real filenames exactly. | `images/*`, `index.html`, `showroom.html` |
| 3 | README described a multi-page site, but the ZIP had only `index.html` with `#anchor` navigation. | Documentation and submission did not match. | Split the site into the six pages listed in the README (`index`, `showroom`, `about`, `heritage`, `ownership`, `contact`). Navigation now links between real pages, and the current page is highlighted with `aria-current`. | all `.html` files |
| 4 | Responsive images were not implemented with `srcset`, `sizes` or `<picture>`. | The CSS only used `max-width: 100%`, so the browser had no alternative resolutions. | Every vehicle image now uses `srcset` (800w and 1600w versions) with a `sizes` attribute, plus `width`/`height` to prevent layout shift and `loading="lazy"` below the fold. Original photos (up to 9.6 MB each) were resized, reducing the image folder from about 35 MB to about 2.7 MB. | `images/*`, `index.html`, `showroom.html` |
| 5 | README referenced `screenshots/desktop.png`, `tablet.png` and `mobile.png`, but the submitted screenshots had different names and only two existed (both about 1900px wide). | Required desktop/tablet/mobile evidence could not be verified. | Added three correctly named screenshots captured at 1440px, 768px and 375px. | `screenshots/*`, `README.md` |
| 6 | No Part 2 changelog documenting lecturer feedback corrections. | The README held iteration notes only. | Added this changelog section. | `README.md` |

### Other improvements made during the rebuild

| Change | Reason | Files affected |
|---|---|---|
| Replaced the pipe-separated (`\|`) navigation with a semantic `<ul>` list | Better accessibility and consistent styling | all `.html` files |
| Added a "Skip to main content" link and a visible focus style | Keyboard accessibility | all `.html`, `css/style.css` |
| Unique `<title>` and meta description for each page | Preparation for Part 3 SEO work | all `.html` files |
| Vehicles shown in a responsive card grid (1, 2 or 3 columns) | Cleaner layout and consistent image sizes (3:2) | `css/style.css`, `showroom.html`, `index.html` |
| Rebuilt the stylesheet with class-based selectors and a mobile-first layout, keeping the original colour variables | Easier to maintain and extend in Part 3 | `css/style.css` |
| Replaced the code-fence characters accidentally left at the end of the old `index.html` | They displayed as text on the page | `index.html` |

### Part 1 feedback corrections
> *(Add the specific Part 1 lecturer feedback and the corrections you made here — the Part 2 feedback says this section was missing. Use the same table format as above.)*

### Part 3 changes
> *(To be completed as Part 3 is built: JavaScript features, dynamic content, SEO, forms and deployment.)*

---

## 3.4 Test and Iterate

### Testing Process
The site was tested using **Chrome Developer Tools (Device Toolbar)** and by opening the final folder directly (not just the development copy) to confirm every CSS, image and page link resolves.

### Testing Observations

**Desktop (1440px)** — three-column vehicle grid, horizontal navigation, full-width hero.

**Tablet (768px)** — two-column grid, navigation remains horizontal.

**Mobile (375px)** — single-column layout, navigation wraps, images scale to fit with no horizontal scrolling, form fields are full width.

### Responsive Breakpoints

| Breakpoint | Target |
|---|---|
| Default | Mobile (single column) |
| `min-width: 768px` | Tablet and up |
| `min-width: 1024px` | Desktop and up |
| `min-width: 1440px` | Large desktop |

### Screenshot Evidence

**Desktop View (1440px)**

![Desktop View](screenshots/desktop.png)

**Tablet View (768px)**

![Tablet View](screenshots/tablet.png)

**Mobile View (375px)**

![Mobile View](screenshots/mobile.png)

### Iteration Notes
1. **Mobile navigation** — list items wrap and keep a 44px touch target.
2. **Image scaling** — `srcset`/`sizes` plus `aspect-ratio` and `object-fit: cover` prevent overflow and distortion.
3. **Form usability** — inputs are `width: 100%` for easier touch use.
4. **Contrast** — muted text and placeholder colours were lightened to improve contrast on the dark background.
5. **Submission check** — the final folder is tested directly before it is zipped and uploaded.

---

## References
> *(Add your updated list of references here, e.g. image sources and any tutorials or documentation you used. Do not leave this empty — the brief asks for an updated reference list.)*

---

© 2026 Velora Motors. All Rights Reserved.
