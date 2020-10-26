# Conference template

Created using modified [hugo-universal-theme](https://github.com/devcows/hugo-universal-theme). See the [demo web site](https://themes.gohugo.io/theme/hugo-universal-theme/), the original [github repository](https://github.com/devcows/hugo-universal-theme) and the [exampleSite files](https://github.com/devcows/hugo-universal-theme/tree/master/exampleSite). Template by [Bootstrapious](https://bootstrapious.com/p/universal-business-e-commerce-template). Ported to Hugo by [DevCows](https://github.com/devcows/hugo-universal-theme).

The theme is added as selected files, not as a submodule, for easier modification.

Clone and, assuming [hugo](https://gohugo.io/getting-started/installing/) is installed, run 
```
rm -rf public; hugo --verbose; hugo server --disableFastRender --verbose
```

Host your site on [Netlify](https://www.netlify.com/), as described [here](https://bookdown.org/yihui/blogdown/netlify.html). Use build command `hugo`, publish directory `public`, and set advanced variable `HUGO_VERSION` to your `hugo version` number, e.g., 0.76.5

# Highlights

- Optimal rendering on desktop and mobile devices
- Overall color theme (default - blue)
- Navigation - menus and conference logo. Tweak logos in `static/img/logo*`
- Carousel - auto-rotating text with images. Tweak in `data/carousel`, `static/img/carousel`
- Sponsors - client/sponsor logos and URLs. Tweak in `data/clients`, `static/img/clients`
- Speakers - speakers with brief bio. Tweak in `data/speakers/`, `static/img/speakers`

# Files

- `config.toml` - main configuration file
    - `menu.main` - menu parameters
    - `menu.topbar` - icons and URLs for contact information
    - Toggle partials to be included
    - about us, copyright, other conference information at the footer

```
archetypes/
└── default.md - default template for creating new content. See [Archetypes](https://gohugo.io/content-management/archetypes/)
```

Content files

```
content/
├── blog - a folder with several posts to get started with Hugo, or transition from Jekyll
├── posts - actual posts are stored here
│   └── my-first-post.md
├── code.md - code of conduct template, opens via menu `code of conduct`
├── contact.md - contacts template, opens via menu `contact`, included in the `contact.html` partial.
└── schedule.md - schedule as Markdown table
```

Customization settings for partials

```
data
├── carousel - auto-rotating text with images. Tweak in data/carousel, static/img/carousel
│   ├── multipurpose1.yaml
│   └── multipurpose2.yaml
├── clients - client/sponsor logos and URLs. Tweak in data/clients, static/img/clients
│   ├── 1.yaml
│   ├── ...
│   └── 6.yaml
├── features - feature highlights. Not used. See demo at https://themes.gohugo.io/theme/hugo-universal-theme/
│   ├── consulting.yaml
│   ├── email.yaml
│   ├── print.yaml
│   ├── seo.yaml
│   ├── uiux.yaml
│   └── webdesign.yaml
└── speakers - speakers with brief bio. Tweak in data/speakers/, static/img/speakers. Originally, testimonials
    ├── 1.yaml
    ├── 2.yaml
    ├── 3.yaml
    ├── 4.yaml
    ├── 5.yaml
    ├── 6.yaml
    └── 7.yaml
 ```

Immutable data for partials

```
static/
└── img
    ├── banners - images for background images for the carousel
    │   ├── banner-1.jpg
    │   ├── banner-2.jpg
    │   ├── banner-3.jpg
    │   ├── banner-4.jpg
    │   └── banner-5.jpg
    ├── carousel - images for carousel, corresponding to YAML files in data/carousel
    │   ├── template-easy-code.png
    │   └── template-tablets.png
    ├── clients - images for sponsors/clients, corresponding to YAML files in data/clients
    │   ├── customer-1.png
    │   ├── customer-2.png
    │   ├── customer-3.png
    │   ├── customer-4.png
    │   ├── customer-5.png
    │   └── customer-6.png
    ├── speakers - images for speakers, corresponding to YAML files in data/speakers
    │   ├── person-1.jpg
    │   ├── person-2.jpg
    │   ├── person-3.png
    │   └── person-4.jpg
    ├── logo-small.png - logos for the navigation bar
    ├── logo.png
    ├── photogrid.jpg - background image for carousel
    ├── texture-bw.png - background textures
    ├── texture-green.png
    ├── texture-turquoise.png
    └── texture-violet.png
```

Partials. Only those that are used have comments

```
themes/hugo-universal-theme/layouts/
├── _default 
│   ├── list.html
│   └── single.html
├── archetypes
│   └── default.md
├── page
│   └── single.html - template for all non-index pages
├── partials
│   ├── widgets
│   │   ├── categories.html
│   │   ├── search.html
│   │   └── tags.html
│   ├── breadcrumbs.html
│   ├── carousel.html - layout of carousel image slider can be adjusted here
│   ├── clients.html - layout for clients/sponsors
│   ├── contact.html - layour for contact form. Includes content/contact.md content
│   ├── features.html
│   ├── footer.html - footer partial. Copyright info should be kept there
│   ├── head.html - header layout, Bootstrap, FontAwesome CSS imports 
│   ├── map.html - included in contact.html, needs authorisation key in config.toml
│   ├── nav.html - navigation panel, with menus. logos are defined in config.toml and in static/img/logo*
│   ├── page.html 
│   ├── recent_posts.html
│   ├── scripts.html
│   ├── see_more.html
│   ├── sidebar.html
│   ├── speakers.html - modified after testimonials.html partial
│   ├── testimonials.html
│   └── top.html - top layout
├── 404.html
└── index.html - front page with all partials. All current news can be added there.
```

CSS styles. Overall color theme can be defined in `config.toml`

```
themes/hugo-universal-theme/static/css
├── animate.css
├── custom.css
├── owl.carousel.css
├── owl.theme.css
├── style.blue.css
├── style.default.css
├── style.green.css
├── style.marsala.css
├── style.pink.css
├── style.red.css
├── style.turquoise.css
└── style.violet.css
```

# ToDo/Help wanted

- Make partials for current news. Currently, they are added directly to `layouts/index.html`

- Make schedule as a partial, populated from `config.toml`. Example - [hugo-conference](https://themes.gohugo.io/hugo-conference/) theme.
