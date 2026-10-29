# Architecture Overview

This repository hosts a static personal website served through GitHub Pages. The architecture is intentionally simple and reliable, with content stored in the GitHub repository and published automatically via GitHub Pages.

```mermaid
flowchart LR
    User[Website Visitor\nBrowser] --> DNS[GitHub Pages Domain\nazizihamid199-hub.github.io]

    DNS --> Pages[GitHub Pages\nStatic Hosting]

    Repo[GitHub Repository\nSource Files] -->|stores content and assets| Pages

    Repo --> HTML[HTML Pages\nindex.html, layouts, content]
    Repo --> CSS[Stylesheets\nCSS, themes, responsiveness]
    Repo --> Assets[Images / Icons / Media]
    Repo --> JS[JavaScript\nUI interactions and behavior]

    HTML -->|renders| User
    CSS -->|styles| User
    JS -->|interacts with| User
    Assets -->|visual content| User

    Pages -->|serves published files| User

    subgraph Site[Personal Site Architecture]
        HTML
        CSS
        JS
        Assets
    end
```

## Overview

- Source content lives in the GitHub repository.
- GitHub Pages publishes the static site to the public domain.
- The browser requests the page through the GitHub Pages endpoint.
- HTML, CSS, JavaScript, and media assets are delivered as static files.
- This architecture is ideal for a portfolio, personal landing page, or lightweight content site with no backend required.
