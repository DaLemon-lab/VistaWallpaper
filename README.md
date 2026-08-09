# Vista

Vista is a marketplace for premium wallpapers and live wallpapers, built for anyone who wants their screen to stand out. Browse a genre organized collection spanning nature, abstract, space, anime, and dark aesthetics, in both static and animated formats for phone and PC. Buy wallpapers individually or subscribe for full genre access.

This is a **single-file demo web app** (`vista.html`). It runs entirely in the browser with no backend server, no build step, and no external dependencies beyond a Google Fonts import.

## Features

- **Browse and search** wallpapers by name, description, or genre, with a live sidebar genre filter.
- **Static and live wallpapers**, uploaded as PNG or MP4, with separate phone and PC versions and per-wallpaper max resolution info.
- **Buy or unlock for free**, either by purchasing a wallpaper individually or getting it for free through a subscription plan.
- **Subscriptions** with a name, icon, monthly price, and description, manageable by admins.
- **Accounts**, with sign up / sign in, a private account page showing purchases and subscription status, and simulated (non-real) payments.
- **Top banner ad**, shown above the header, using a PNG or MP4 the admin uploads, linking out to any URL when clicked.
- **Website Settings panel** (admin only) for changing the site logo, managing the top banner ad, deleting wallpapers, and managing genres.
- **Light / dark theme** toggle, saved per browser.
- **Download flow** that lets the user pick a save location (where supported) and choose between phone and PC versions.

## Getting Started

No install or build required.

1. Download `wallstore.html`.
2. Open it directly in a modern browser (Chrome, Edge, or Firefox recommended).

That's it. The app loads and saves all of its data locally in the browser.

## Admin Access

The account with the email set in `ADMIN_EMAIL` (near the top of the `<script>` block) is always an admin and cannot be demoted. Admins can:

- Add and delete wallpapers
- Create and delete subscription plans
- View the list of everyone who has logged in, and promote/demote other admins
- Open **Website Settings** (🛠 Website) to:
  - Change the site logo
  - Upload, replace, or remove the top banner ad and its click-through link
  - Delete wallpapers
  - Add or delete genres

To make another account an admin, sign in as the primary admin, go to **Users**, and click **Make admin** next to their name.

## Data Storage

All data (users, wallpapers, subscriptions, genres, logo, ad, and theme) is stored in the browser's **IndexedDB**, scoped to the device and browser it was created in. There is no server and no shared database.

This means:
- Data does not sync across devices or browsers.
- Clearing browser storage / site data will erase everything.
- Passwords are stored as plain text in local storage. **Do not use a real password you use elsewhere.**

## Known Limitations

- Login, payments, and file protection are simulated for demonstration purposes only. They are not a substitute for a real backend, authentication provider, or payment processor.
- Large image/video uploads are stored as base64 data URLs, which can hit browser storage limits on very large files.
- No real user privacy, security hardening, or backup strategy is included.

## Tech Stack

- Plain HTML, CSS, and vanilla JavaScript (no framework)
- Google Fonts (Sora, Inter)
- Browser `IndexedDB` for persistence

## File Structure

```
wallstore.html   # the entire application: markup, styles, and logic
```

## License

Internal / demo project. Add a license here if you plan to distribute this.
