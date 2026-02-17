# Index

What is the index in plain html? This is the landing page, the starting point, the center node holding the entire graph together.

How is this configd in Astro's routing? Astro uses "file-based routing", which just means static routes (direct mapping between a file on your disk and a URL in the browser.) are built automatically for every .astro, .md, or .mdx file under the `src/pages` dir.

Here, index.astro is the default, as for every other website. I think it probably dates back to the history when CERN built it, but not completely sure how this is enforced. You can customize this via `build.format`

> "There is no separate “routing config” to maintain in an Astro project! When you add a file to the src/pages/ directory, a new route is automatically created for you. In static builds, you can customize the file output format using the build.format configuration option." - [Astro Doc (Static routes)](https://docs.astro.build/en/guides/routing/#static-routes)
