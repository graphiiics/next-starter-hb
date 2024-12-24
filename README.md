This is a [Next.js](https://nextjs.org) project bootstrapped with
[`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the
result.

You can start editing the page by modifying `app/page.js`. The page auto-updates
as you edit the file.

This project uses
[`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts)
to automatically optimize and load [Geist](https://vercel.com/font), a new font
family for Vercel.

## Learn More (Notes by Me | )

### Your first app

#### Create a NextJs app

1. We create the project in a previous folder with the following command and
   selecting these settings:

```bash
pnpx create-next-app@latest .

Progress: resolved 1, reused 0, downloaded 1, added 1, done
✔ Would you like to use TypeScript? … No
✔ Would you like to use ESLint? … Yes
✔ Would you like to use Tailwind CSS? … Yes
✔ Would you like your code inside a `src/` directory? … No
✔ Would you like to use App Router? (recommended) … Yes
✔ Would you like to use Turbopack for `next dev`? … No
✔ Would you like to customize the import alias (`@/*` by default)? … Yes
✔ What import alias would you like configured? … @/*
Creating a new Next.js app in /Users/gaelmanzanares/Code/next-starter-hb.
```

2. Change the extension for to layout.js and page.js to "jsx"

3. Remove the content of the page.jsx and apply a custom one.

4. Remove the default theme in tailwind.config.js and apply this one:

```json
theme: {
    container: {
      center: true,
      padding: "1rem",
      md: "1.5rem",
      lg: "2rem",
    },
  },
```

5. Remove the default code in app/globals.css and just leave the following:

```javascript
@tailwind base;
@tailwind components;
@tailwind utilities;
```

6. Apply the Automatic Class Sorting with Prettier

First install plugin

```bash
pnpm install -D prettier prettier-plugin-tailwindcss
```

Then create the .prettierrc with these settings:

```bash
{
  "arrowParens": "avoid",
  "singleQuote": true,
  "jsxSingleQuote": true,
  "tabWidth": 2,
  "trailingComma": "none",
  "semi": false,
  "proseWrap": "always",
  "printWidth": 80,
  "plugins": ["prettier-plugin-tailwindcss"]
}
```

⚠️ Important to have installed the prettier extension.
