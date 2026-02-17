# Components

## Headers

Defines `<header>` with `<nav>`. `<nav>` uses `<Menu>` and `<Navigation>` component.

Also some footer style here for some reason, mb remove?

### Menu

The `<Menu>` component is for the toggle button for mobile.

- Uses a Vanilla JavaScript script to toggle the `aria-expanded `attribute.
- Styling w/ Tailwind CSS `@apply`
- Mobile: Hides links by default by using the CSS `:has()` selector to show them when the button is clicked.
- Desktop: Automatically hides the toggle button and displays links horizontally via media queries.

### Navigation

`"nav-links"` class defined in css used by div container. Body contains link home, about, + blog with `href` point to their respective pages:

- Home = "/" = `src/pages/index.astro`
- About = "/about/" = `src/pages/about.astro`
- Blog = "/blog/" = `src/pages/blog.astro`

## Footer

Defines `<footer>` container which uses `<Social>` component to define each social link e.g. "www.linkedin.com/username".
