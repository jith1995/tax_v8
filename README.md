# Clarity Tax MVP

Static Vercel-ready site for the Clarity ITR filing MVP.

## Structure

- `index.html` - homepage and interactive tax path tool
- `articles/` - SEO guide pages
- `assets/article.css` - shared article page styling
- `vercel.json` - static deployment config

Upload all files to the root of your GitHub repo and connect to Vercel.

## Update: Income-head-wise computation

The live tax tool now separates income-head calculations before applying common deductions. This is to reflect CA feedback that salary, house property, capital gains and other sources have different deduction mechanics.

Key addition: rental income is calculated under House Property using gross rent, municipal taxes, 30% standard deduction and home-loan interest inputs.


## Split page update

The homepage (`index.html`) is now a clean landing page with preview cards and SEO content. The full working wizard has moved to `tax-tool.html`. Keep both files in the repo root for Vercel.
