# fonts

See [releases](https://github.com/MohammadRaziei/fonts/releases)


### Github actions

```
  - name: Download Fonts
    uses: robinraju/release-downloader@v1.8
    with:
      tag: "fa-Latex"
      # Choose what fonts you need from https://github.com/MohammadRaziei/fonts/releases
      repository: "mohammadraziei/fonts"
      fileName: "fonts.zip"
      out-file-path: "fonts"
      extract: true
```
