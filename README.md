# Thomas Ayman: Portfolio Website

A React + Vite portfolio for Thomas Ayman, HR Generalist | HR Data Analyst.

Stack: React 18, Framer Motion, Recharts, Lucide React, plain CSS (organized in `src/index.css`).

## Run it

Requires Node.js 18 or newer.

```bash
npm install
npm run dev      # development server at http://localhost:5173
npm run build    # production build in dist/
npm run preview  # preview the production build
```

## Things to personalize

| What | Where |
| --- | --- |
| Profile photo | Save a photo as `src/assets/profile.jpg` (also `.jpeg`, `.png`, `.webp`). It replaces the placeholder in the hero and About sections automatically. A portrait about 800 x 920 px works well. |
| Email, LinkedIn, WhatsApp | `contactInfo` in `src/data/content.js`. Fill in `display` and `href` (for example `mailto:name@example.com`, a LinkedIn URL, or `https://wa.me/<number>`). Until `href` is set, the item shows as a non-clickable placeholder. |
| All other text, services, achievements, skills | `src/data/content.js` |
| Colors and spacing | CSS variables at the top of `src/index.css` |
| Page title and description | `index.html` |

## Contact form

The form validates all four fields and shows loading, success, and error states, but this project has no backend, so **no email is sent yet**. While `IS_DEMO` is `true` in `src/services/sendMessage.js`, the success message says so.

To send real messages, edit `src/services/sendMessage.js`. The file contains ready-to-adapt examples for Formspree and EmailJS. After connecting a service, set `IS_DEMO` to `false`.

## Content accuracy

All figures come from the supplied brief (2,500+ employees, 30% efficiency improvement, 35% reduction in role ambiguity, 45% performance increase). The 45% figure is intentionally not tied to a specific metric. The small trend line in the hero is decorative and carries no data. No testimonials, logos, case studies, or contact details were invented.

## Project structure

```
src/
  components/   Navbar, Hero, About, Services, Achievements, Skills,
                Courses, Contact, Footer + shared pieces (Reveal, StatCard, ...)
  data/         content.js (all editable content)
  hooks/        useActiveSection, useCountUp
  services/     sendMessage.js (contact form delivery)
  assets/       put profile.jpg here
  App.jsx, main.jsx, index.css
```

## Accessibility notes

Skip link, visible keyboard focus, labelled form fields with inline errors, `aria-current` on the active nav link, external links that announce "opens in a new tab", and `prefers-reduced-motion` respected for scrolling, reveals, and counters.
