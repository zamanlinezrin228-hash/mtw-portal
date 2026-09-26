# MARS Talent Wise (MTW)

Talent Development Ecosystem portal for Mars Overseas Baku LTD.

## Files
- `index.html` – the whole portal (design, logic, module links)
- `assets/logo-mark.svg` – MTW icon (app icon, favicon, Teams tab icon)
- `assets/logo-full.svg` – icon + "MARS Talent Wise" wordmark

## Adding the Recruitment and AI Chatbot links
Open `index.html`, find `const MODULES = [` and fill in `url: ""`:

    url: "https://your-recruitment-app.vercel.app/",
    mode: "embed",

- `embed` shows the tool inside the portal window.
- `launch` opens it in a new tab (needed for SharePoint / Microsoft 365, which block embedding).

Commit the change on GitHub – Vercel redeploys automatically in ~30 seconds.

## Deploy: GitHub -> Vercel
1. github.com -> New repository -> name `mtw-portal` -> Private -> Create.
2. "uploading an existing file" -> drag `index.html`, `README.md` and the `assets` folder -> Commit.
3. vercel.com -> Add New -> Project -> Import `mtw-portal`.
4. Framework Preset: Other. Leave build command and output directory empty -> Deploy.
5. Optional: Project -> Settings -> Domains -> add e.g. `talent.marsoverseas.az` and add the DNS record Vercel shows.

## Supabase
Not needed for this version (static site, no database).
Add it later for: employee login, saving recruitment data, chatbot history, usage statistics.
Store keys in Vercel -> Settings -> Environment Variables, never in index.html.
