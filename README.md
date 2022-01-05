<!--- CARD BEGIN --->

![DNB-Hugo/HEAD](.github/github-card-dark.png#gh-dark-mode-only)
![DNB-Hugo/HEAD](.github/github-card-light.png#gh-light-mode-only)

<!--- CARD END --->

# DNB GoHugo Component / Workflows

A collection of Github Actions/Workflows to optimise your work with GoHugo.

❗work in progress. open a PR or an issue with questions.

## Setup Workflows

### [update-netlify.yml](.github/workflows/update-netlify.yml)

- **Schedule:** weekly or monthly
- **Reasoning:** Hugo every now and then receives updates with new features and bug fixes. Netlify offers hugo, but without configuration of the Hugo version to use it will fall back to a very old version (one that does not offer pipes or any of the newer features added in the past two three years). This workflow checks for the latest Hugo version and opens a PR to update your netlify.toml with the latest Hugo version.

## Code Quality Workflows

![https://imgs.xkcd.com/comics/code_quality.png](https://imgs.xkcd.com/comics/code_quality.png)

To be written.
