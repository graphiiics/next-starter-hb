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

### 2. Your first app

#### 2.1 Create a NextJs app

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

```json
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

### 2.2 Styling

1. Beside to use tailwind to styling our components also with can use the
   alternative to create alternatives as:

- Global CSS
- CSS Modules

2. Global CSS is basically describe rules on the global css.

3. CSS Modules is create files with extension .module.css that will apply only
   in specific components or pages.

```javascript
import styles from './page.module.css'
export default function Home() {
  return (
    <section>
        <h1 className={styles.title}>Next 15.1.2 Starter
    </section>
  )
}
```

4. There some libraries that we can use with previous components styled, for
   example:

- Tailwind ui
- Headless ui
- Radix

### 2.3 Deploy your app

```bash
pnpm build
```
