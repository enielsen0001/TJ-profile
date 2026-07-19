
# Tiffany Jones · Life Insurance Specialist Profile

A lightweight, high-performance, single-page profile website built using a modern **Git-based CMS architecture**. The site layout is completely locked down in code, while all copy and text blocks are safely decoupled into local JSON files, enabling seamless updates for non-technical users without a database.

## The Tech Stack

- **Frontend:** [Astro](https://astro.build/) (Static Site Generation for instantaneous load speeds)
- **Styling:** [Tailwind CSS v4](https://tailwindcss.com/) (Utility-first styles with native CSS variable theme configuration)
- **Icons:** [@lucide/astro](https://lucide.dev/) (Native featherweight SVG icons)
- **CMS Layer:** [Sveltia CMS](https://github.com/sveltia/sveltia-cms) (An open-source, client-side, Git-based content management dashboard)
- **Hosting & Auth:** [Netlify](https://www.netlify.com/) + Netlify Identity (Free static hosting with secure, database-free email authentication)

---

## Developer Workflow

### Local Development

1. **Install Dependencies:**
   ```bash
   npm install

```

2. **Start the Development Server:**
```bash
npm run dev

```


Open `http://localhost:4321/` to view the site locally.
3. **Local Content Dashboard:**
Navigate to `http://localhost:4321/admin/` to launch the local Sveltia CMS instance. Local file-system modifications made here will rewrite `src/data/homepage.json` and `src/data/privacy.json` instantly in your workspace.

### Project Architecture

```text
├── src/
│   ├── data/
│   │   ├── homepage.json      <-- Editable text variables for the landing page
│   │   └── privacy.json       <-- Editable text variables for the privacy policy
│   ├── pages/
│   │   ├── admin.astro        <-- Secure CMS entry point dashboard route
│   │   ├── index.astro        <-- Main Figma-ported landing page layout
│   │   └── privacy-policy.astro <-- Dynamic Privacy Policy page route
│   └── styles/
│       └── global.css         <-- Tailwind v4 theme variables & base typography layer
├── public/
│   ├── admin/
│   │   └── config.yml         <-- CMS form-field mappings to JSON variables
│   └── imports/               <-- Static asset folder for profile headshots/images

```

---

## How to Edit Content (For Tiffany)

You don't need to know how to code, use GitHub, or open a terminal to update your website. Your changes will go live automatically in less than a minute.

### Step-by-Step Updates:

1. **Log In:**
Go to your live website URL and add `/admin` to the end of the address bar (e.g., `yourdomain.com/admin`). Log in using your secure email address and password.
2. **Choose a Page:**
On the left sidebar, click on **Website Pages**. You will see two options:
* **Homepage Content:** Controls the headline, biography, buttons, and call-to-action sections of your main profile page.
* **Privacy Policy Page:** Controls the legal text and effective date of your privacy disclosure.


3. **Update the Text:**
Click on the page you want to edit. You will be presented with a simple, clean form containing clear boxes like `Hero Title`, `Hero Biography Text`, and `Tagline`. Type your changes directly into these boxes.
4. **Publish Your Changes:**
When you are happy with your edits, click the green **Publish** button at the top right of the dashboard.

### What Happens Behind the Scenes:

When you click Publish, the system securely logs your text changes into your private project files and signals your hosting provider (Netlify). Netlify will instantly rebuild your website with your new changes. **Your updates will be live on the internet within 10 to 15 seconds.**

