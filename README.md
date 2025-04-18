# Researcher

A simple monospaced resume theme for Hugo. It was ported from Jekyll theme
[ankitsultana/researcher](https://github.com/ankitsultana/researcher).

## Screenshot
![screenshot](https://user-images.githubusercontent.com/23409060/188607083-dd087121-16f9-4706-b8b9-a0e4c9e35d93.png)

## Installation
This theme uses Sass to generate CSS files so make sure you have the
*extended* Hugo version installed.

Add the theme to your site's `themes` directory:
```bash
git submodule add https://github.com/ojroques/hugo-researcher.git themes/researcher
# if your website is not managed by git:
# git clone https://github.com/ojroques/hugo-researcher.git themes/researcher
```

Update the theme option in `config.toml`:
```toml
theme = "researcher"
```

## Configuration
A self-explanatory configuration file is present in
[exampleSite/config.toml](https://github.com/ojroques/hugo-researcher/blob/master/exampleSite/config.toml),
along the files of a demo website.

### Dark Mode
The theme supports dark mode through:
- Automatic detection of system preferences
- A manual toggle button in the navigation bar
- Persistence of user preference via localStorage

To customize dark mode colors, update your `config.toml`:
```toml
[params.style]
  colorBlack = "#222222"    # Main text color in light mode
  colorRed = "#dc3545"      # Accent color in light mode
  colorRedDark = "#ff6b6b"  # Accent color in dark mode
```

## KaTeX
You can enable [KaTeX](https://katex.org/) (math typesetting) by including
`math: true` in your content files. Or you can enable it globally by setting
`math` to `true` in your project config.

Hugo introduces tags when it sees newlines which breaks KaTeX block
environments. The theme has a `math` shortcode to circumvent this issue:
```md
{{< math >}}
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
{{< /math >}}
```
Check [this
issue](https://github.com/ojroques/hugo-researcher/issues/1#issuecomment-697247056)
for more details.

## License
[GPL-3.0 License](https://github.com/ojroques/hugo-researcher/blob/master/LICENSE)
