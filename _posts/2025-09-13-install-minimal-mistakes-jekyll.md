
# Install [minimal-mistakes-jekyll](https://github.com/mmistakes/minimal-mistakes?tab=readme-ov-file)
> Minimal Mistakes is a flexible two-column Jekyll theme, perfect for building personal sites, blogs, and portfolios. As the name implies, styling is purposely minimalistic to be enhanced and customized by you 😄.

\* **Prerequisites**: Have Ruby and Gem installed.

## Install [Jekyll](https://github.com/jekyll/jekyll)

```bash
gem install jekyll
```

### Initialize jekyll project
```bash
jekyll new . --force
```

### Install theme
1. Create/replace the contents of your Gemfile with the following:

    ````bash
    source "https://rubygems.org"

    gem "github-pages", group: :jekyll_plugins
    gem "jekyll-include-cache", group: :jekyll_plugins
    ````
2. Add `- jekyll-include-cache` to the plugins array of your `_config.yml`.

3. Fetch and update bundled gems by running the following Bundler command:

    ```bash
    bundle
    ```
4. Add remote_theme: "mmistakes/minimal-mistakes@4.27.3" to your _config.yml file. Remove any other theme: or remote_theme: entry


