<!--- CARDS BEGIN --->

![DNB-Hugo/TEMPLATES](.github/github-card-dark.png#gh-dark-mode-only)
![DNB-Hugo/TEMPLATES](.github/github-card-light.png#gh-light-mode-only)
<!--- CARDS END --->

# DNB GoHugo Component / Workflows

A collection of Github Actions/Workflows to optimise your work with GoHugo.

This is not a copy/paste repository but a collection of workflows [I](https://github.com/davidsneighbour) am using on my own projects. You can copy and paste, then read through the scripts and setups and adapt to your own requirements. I try to explain the procedures as verbose as possible. Feel free to open an issue if you require more information or a specific workflow that I did not include yet.

❗work in progress. open a PR or an issue with questions.

## Setup Workflows

### [update-netlify.yml](.github/workflows/update-netlify.yml)

- **Feature:** This workflow checks for the latest published Hugo version and opens a PR to update your netlify.toml with the latest Hugo version.
- **COPY/PASTEable**: No, change to your required setup
- **Requirements:** [bin/update-hugo-on-netlify.sh](bin/update-hugo-on-netlify.sh) and [workflow configuration](.github/workflows/update-netlify.yml)
- **Schedule:** daily at midnight (default), try weekly or monthly
- **Reasoning:** Hugo every now and then receives updates with new features and bug fixes. [Netlify](https://www.netlify.com/) offers Hugo, but without configuration of the Hugo version to use it will fall back to a very old version (one that does not offer pipes or any of the newer features added in the past two three years).

The [workflows](.github/workflows/update-netlify.yml) configuration sets the `cron` variable of the [schedule](https://docs.github.com/en/actions/learn-github-actions/events-that-trigger-workflows#schedule) to daily runs at midnight of your repositories timezone. Use [crontab.guru](https://crontab.guru/) to create a setup that fits your needs. I would suggest a weekly (`@weekly`) or monthly (`@monthly`) run.

Have a look into the [bin/update-hugo-on-netlify.sh](bin/update-hugo-on-netlify.sh) and update the template according to your netlify.toml setup. The important thing is to keep the line `HUGO_VERSION = "${1/v/""}"` in all sections where you require to set the Hugo version.

[Read more about how to use Hugo on Netlify](https://docs.netlify.com/configure-builds/common-configurations/hugo/).

---

## Code Quality Workflows

![https://imgs.xkcd.com/comics/code_quality.png](https://imgs.xkcd.com/comics/code_quality.png)

To be written.

<!--- COMPONENTS BEGIN --->
## Other [GoHugo](https://gohugo.io/) components by [@dnb-org](https://github.com/dnb-org/)

<!-- prettier-ignore -->
| Component | Description |
| :--- | :--- |
| [dnb-hugo-auditor](https://github.com/dnb-org/dnb-hugo-auditor) | |
| [dnb-hugo-debug](https://github.com/dnb-org/dnb-hugo-debug) :mage_man: | |
| [dnb-hugo-errors](https://github.com/dnb-org/dnb-hugo-errors) | |
| [dnb-hugo-feeds](https://github.com/dnb-org/dnb-hugo-feeds) | Implements various configurable feed formats. |
| [dnb-hugo-functions](https://github.com/dnb-org/dnb-hugo-functions) | |
| [dnb-hugo-giscus](https://github.com/dnb-org/dnb-hugo-giscus) | The Giscus comment system layout for GoHugo. |
| [dnb-hugo-head](https://github.com/dnb-org/dnb-hugo-head) | A GoHugo theme component that solves the old question of "What tags belong into the `<head>` tag of my website?" |
| [dnb-hugo-hooks](https://github.com/dnb-org/dnb-hugo-hooks) | GoHugo's missing hook system for template extensions. |
| [dnb-hugo-humans](https://github.com/dnb-org/dnb-hugo-humans) | Your site is made by humans. Humans.txt is naming them. |
| [dnb-hugo-internals](https://github.com/dnb-org/dnb-hugo-internals) | Better internal templates for GoHugo |
| [dnb-hugo-netlification](https://github.com/dnb-org/dnb-hugo-netlification) | a collection of tools that optimize your site on Netlify |
| [dnb-hugo-opensearch](https://github.com/dnb-org/dnb-hugo-opensearch) | configuration for Open Search |
| [dnb-hugo-pictures](https://github.com/dnb-org/dnb-hugo-pictures) | |
| [dnb-hugo-pwa](https://github.com/dnb-org/dnb-hugo-pwa) | Automatically turns your site into a PWA |
| [dnb-hugo-renderhooks](https://github.com/dnb-org/dnb-hugo-renderhooks) | render hooks for Markdown markup |
| [dnb-hugo-robots](https://github.com/dnb-org/dnb-hugo-robots) | configure the content of your robots.txt with front matter |
| [dnb-hugo-schema](https://github.com/dnb-org/dnb-hugo-schema) | |
| [dnb-hugo-search-algolia](https://github.com/dnb-org/dnb-hugo-search-algolia) | |
| [dnb-hugo-security](https://github.com/dnb-org/dnb-hugo-security) | |
| [dnb-hugo-sitemap](https://github.com/dnb-org/dnb-hugo-sitemap) | |
| [dnb-hugo-social](https://github.com/dnb-org/dnb-hugo-social) | |
| [dnb-hugo-workflows](https://github.com/dnb-org/dnb-hugo-workflows) | A collection of Github Actions/Workflows to optimise your work with GoHugo. |
| [dnb-hugo-youtube](https://github.com/dnb-org/dnb-hugo-youtube) | A shortcode and partial for lite youtube embeds. |





<!--lint disable no-missing-blank-lines -->
<!--- COMPONENTS END --->
