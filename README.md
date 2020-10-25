# Conference template

Created using modified [hugo-universal-theme](https://github.com/devcows/hugo-universal-theme)

```
archetypes/
└── default.md - default template for creating new content. See [Archetypes](https://gohugo.io/content-management/archetypes/)
```

```
content/
├── blog - a folder with several posts to get started with Hugo, or transition from Jekyll
├── posts - actual posts are stored here
│   └── my-first-post.md
├── code.md - code of conduct template, opens via menu `code of conduct`
├── contact.md - contacts template, opens via menu `contact`, included in the `contact.html` partial.
└── schedule.md - schedule as Markdown table
```

# ToDo/Help wanted

- Make schedule as a partial, populated from `config.toml`. Example - [hugo-conference](https://themes.gohugo.io/hugo-conference/) theme.
