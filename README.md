# DSP Forge Marketing Site

Static marketing site for DSP Forge, designed for fast deployment anywhere.

## Files

- `index.html` - landing page
- `features.html` - product capabilities
- `pricing.html` - pricing and custom development
- `about.html` - founder story and mission
- `contact.html` - contact form and direct email CTA
- `styles.css` - shared site styling
- `assets/` - copied product screenshots used throughout the site

## Deployment

Because this is a static site, you can deploy it almost anywhere.

### Option 1: Netlify / Vercel static upload
1. Point the hosting provider at `marketing-site/`
2. Set the publish directory to `marketing-site`
3. No build command is required

### Option 2: GitHub Pages
1. Commit the `marketing-site/` folder
2. Serve it from the repo root or copy it into your docs/site publishing path
3. Make sure `index.html` stays at the deployed root

### Option 3: Any web server
Upload the full `marketing-site/` folder contents to your web root.

## Pages and key copy

### Home
- Hero: "Built by a dispatcher who got tired of spreadsheets"
- Positioning: Amazon DSP software for hours tracking, scheduling, attendance, and custom workflows
- Social proof: built for a 70-driver DSP
- Pricing anchor: $3 to $4 per driver per month vs competitors at $10 to $12
- CTAs: "Try the demo" and "Contact for custom features"

### Features
- Hours tracking with DOT compliance alerts
- Schedule builder with 2-week projections
- Attendance reporting
- Mobile-responsive layout
- Offline support
- Custom development availability

### Pricing
- Core plan at $3 to $4 per driver per month
- Included features list
- Custom development options, hourly or fixed project
- Enterprise and white-label CTA

### About
- Founder story based on 4 years as a dispatcher
- Mission: DSPs deserve better software
- Photo placeholder ready to replace with real image

### Contact
- Simple contact form using mailto
- Direct email CTA for demos and custom requests

## Screenshot placements

- `index.html`
  - Dashboard
  - Schedule builder
  - Attendance report
  - Hours report
- `features.html`
  - Schedule builder hero support
  - Dashboard
  - Hours report
  - Attendance report
  - Login screen
- `pricing.html`
  - Hours report
- `about.html`
  - Dashboard

## Notes

- Contact email is currently `hello@dspforge.com` as a placeholder. Replace it if needed.
- Founder image is still a placeholder block in `about.html`.
- If you want a real contact backend later, swap the `mailto:` form for Formspree, Basin, Netlify Forms, or a simple server endpoint.
