# fistbumpz E-Sports Team Website

## Project Overview
Single-page website for the fistbumpz e-sports team. This is a static site designed to be hosted on GitHub Pages.

## Tech Stack
- **Pure HTML/CSS/JS** - Single `index.html` file, no build process
- **Hosting** - GitHub Pages
- **Design** - Dark gaming theme inspired by nutorious.gg

## Architecture

### File Structure
- `index.html` - Complete single-page website with embedded CSS and JavaScript
- No external dependencies or build tools required

### Design System
The site uses CSS custom properties (variables) defined in `:root` for easy customization:
- `--bg-dark`: Main background color (#0a0a0a)
- `--bg-card`: Card background (#1e1e1e)
- `--accent-primary`: Primary accent color (#7c3aed - purple)
- `--accent-secondary`: Secondary accent color (#3b82f6 - blue)
- `--text-primary`: Main text color (#ffffff)
- `--text-secondary`: Secondary text color (#a0a0a0)

### Page Sections (in order)
1. **Hero** - Full viewport height welcome section with gradient logo
2. **About** - Team description and mission (3 paragraphs)
3. **Team Roster** - Grid of player cards (6 members currently)
4. **Social Media** - Icon links to social platforms
5. **Footer** - Copyright and contact email

## Customization Guide

### Updating Colors
Edit the CSS variables at the top of the `<style>` section in `index.html`:
```css
:root {
    --accent-primary: #7c3aed;  /* Change this for primary brand color */
    --accent-secondary: #3b82f6; /* Change this for secondary brand color */
}
```

### Adding/Removing Team Members
Find the `.roster-grid` section and add/remove `.player-card` divs:
```html
<div class="player-card">
    <div class="player-avatar">XX</div>
    <h3>PlayerName</h3>
    <div class="player-role">Role</div>
    <div class="player-game">Game</div>
</div>
```

### Updating Social Media Links
Replace `href="#"` with actual URLs in the `.social-links` section. Icons use emoji placeholders - can be replaced with SVG icons or Font Awesome if needed.

### Adding Real Images
To replace placeholder avatars:
1. Add image files to an `images/` folder
2. Replace `<div class="player-avatar">XX</div>` with:
   ```html
   <img src="images/player-name.jpg" alt="Player Name" class="player-avatar">
   ```
3. Update CSS for `.player-avatar img` if needed

### Replacing Text Logo with Image
Replace the `<h1>fistbumpz</h1>` in the hero section with:
```html
<img src="images/logo.png" alt="fistbumpz" style="max-width: 600px;">
```

## GitHub Pages Deployment
1. Push this repo to GitHub
2. Go to repository Settings → Pages
3. Set Source to "Deploy from a branch"
4. Select branch: `main` (or `master`)
5. Select folder: `/ (root)`
6. Save and wait for deployment
7. Site will be live at: `https://[username].github.io/fistbumpz/`

## Common Modifications

### Change Tagline
Edit line in hero section:
```html
<p>Dominating the competition, one game at a time</p>
```

### Update About Text
Edit the three `<p>` tags in the `.about-content` div

### Change Contact Email
Update footer:
```html
<a href="mailto:contact@fistbumpz.gg">contact@fistbumpz.gg</a>
```

## Design Notes
- Responsive breakpoint at 768px for mobile/tablet
- Smooth scroll enabled via `scroll-behavior: smooth`
- All animations use CSS (no JS animation libraries)
- Gradient backgrounds use linear-gradient for visual interest
- Hover effects on interactive elements for better UX

## Future Enhancement Ideas
- Add a Schedule/Matches section
- Add an Achievements/Trophies section
- Integrate with Twitch API for live stream status
- Add image gallery or highlights section
- Create a sponsors section if applicable
