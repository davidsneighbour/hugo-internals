<!--- CARD BEGIN --->

![DNB-Hugo/INTERNALS](.github/github-card-dark.png#gh-dark-mode-only)
![DNB-Hugo/INTERNALS](.github/github-card-light.png#gh-light-mode-only)

<!--- CARD END --->

# GoHugo Component / Internals

This module replaces internal templates used by Hugo with custom ones and other repositories that add identical features more sophisticated. Internal templates of Hugo are highly opiniated and not suitable for use in the production environment of a website. The layouts in this repo and it's modules replace them with our own better setup. 

## Installing

First enable modules in your own repository:

```bash
hugo mod init github.com/username/reponame
```

Then add this module to your required modules in config.toml.

```toml
[module]
[[module.imports]]
path = "github.com/davidsneighbour/hugo-internals"
```

The next time you run `hugo` it will download the latest version of the module and other modules.

## Updating

```shell
# update this module
hugo mod get -u github.com/davidsneighbour/hugo-internals
# update all modules
hugo mod get -u ./...
```

## Configuration

### robots.txt

This component uses [hugo-robots](https://github.com/davidsneighbour/hugo-robots) to create a robots.txt without much configuration. The only step to take is that robots.txt generation needs to be enabled in your configuration, eg. config.toml:

```toml
enableRobotsTXT = true
```
