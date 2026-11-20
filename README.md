# Document Design System

CSS for blogs, technical documentation, and other reading pages. The theme comes from sorafujitani.me and does not depend on Astro or JavaScript.

## Install

```sh
bun add github:sorafujitani/document-design-system#v0.1.0
```

Import the stylesheets from your app's CSS or JavaScript entry point. Load the tokens before the styles that use them.

```css
@import "@sorafujitani/document-design-system/tokens.css";
@import "@sorafujitani/document-design-system/theme.css";
@import "@sorafujitani/document-design-system/prose.css";
```

```html
<body class="sora-theme">
  <main class="sora-prose">
    <h1>My document</h1>
    <p>Page content goes here.</p>
  </main>
</body>
```

| Stylesheet | When to use it |
| --- | --- |
| `tokens.css` | Use shared colors and fonts in your own styles. Apply `.sora-tokens` to a wrapper if you do not want the theme. |
| `theme.css` | Apply the gradient background and default text styles to an element with `.sora-theme`. This class also enables the tokens. |
| `prose.css` | Apply article styles to headings, lists, links, quotes, code, images, and tables inside `.sora-prose`. Put it inside a theme or token scope. |

Set the page width, outer spacing, and navigation in the consuming app. You can override individual tokens on the scoped element. Syntax highlighting and embed styles are not part of the package.

## Preview

Open [`examples/document.html`](examples/document.html) from a checkout. It links directly to the same stylesheets, so there is no build step.