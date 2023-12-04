# fonts

See [releases](https://github.com/MohammadRaziei/fonts/releases)


### Github actions

```yaml
- name: Download Fonts
  uses: robinraju/release-downloader@v1.8
  with:
    # Choose what fonts you need from https://github.com/MohammadRaziei/fonts/releases
    tag: "Latex-lite"

    # Do not change the following lines
    repository: "mohammadraziei/fonts"
    fileName: "fonts.zip"
    out-file-path: "fonts"
    extract: true
```
