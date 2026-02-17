# Layouts

[_TOC_]

## BaseLayout

This is the pre-defined canvas that each page will live on. According to the official Astro documentation, a layout is a reusable component used to provide a consistent UI structure (a "page shell") across sites. Here we define

- `<html>`: root of each page, doc container.
- `<head>`: metadata for search engines and/or browsers.
- `<body>`: container for all user-visible content.
  - Defines the `<Header />`, `<slot />`, `<Footer />`, and `<h1>` title.
  - `<slot />`: placeholder that tells Astro where to "inject" the specific content from each individual page.
- `Astro.props`: dynamic data passed from pages that use this `layout`. _Not specific to layouts, just wanted to note._

## MarkdownPostLayout

Layout for each blog post `.md`. Each blog post will use the bridge `layout: MarkdownPostLayout.astro`, take the grabs all of the frontmatter YAML vals and formats them into a HTML, then inserts the the actual Markdown body text in the `<slot />`.

## BlogPost

Layout for each blog post URL pointer which lives under `blog.astro`. Rather that repeatedly redefining the list (`<li>`) container with the anchor + URL (`<a href>`) within, we can use this is just inject the URL + text attached over the hyperlink.

```astro
<li><a href={url}>{title}</a></li>
<!------->
<BlogPost url={"www.example.com"} title={"foobar"} />
<!------->
- [foobar](www.example.com)
```
