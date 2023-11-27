# ABCD-J website sources

- The website is built with [hugo](https://gohugo.io/) and uses the [PaperMod](https://themes.gohugo.io/themes/hugo-papermod/) theme.
- Theme is attached as a submodule (supports dark & light mode)
- Content is written in Markdown and placed in `content/`
  - One file corresponds to one page;
    include `menu: "main"` and `weight: N` in front matter to determine placement in the top menu.
- Home page (title, icons, social links) is generated based on configuration only
- Configuration is done with toml, in `config.toml`
- There is a github action for deploying to GitHub pages, which builds to gh-pages branch, which is deployed to the custom domain data.abcd-j.de
- As with any static generator, the content can be built locally and deployed anywhere

### Local development & preview:

```
sudo apt install hugo
git clone --recurse-submodules <repo url>
cd website
hugo server
```