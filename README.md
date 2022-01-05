<!--- CARD BEGIN --->

![DNB-Hugo/HEAD](.github/github-card-dark.png#gh-dark-mode-only)
![DNB-Hugo/HEAD](.github/github-card-light.png#gh-light-mode-only)

<!--- CARD END --->

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
