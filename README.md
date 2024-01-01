# fonts

[![go to images](https://github.com/MohammadRaziei/fonts/raw/master/readme/go-to-fonts-page.jpg)](https://github.com/MohammadRaziei/fonts/releases)


## How to use it.

There is many ways to download the fonts from [releases](https://github.com/MohammadRaziei/fonts/releases). that we covered them in bellow. 

> Each releases has its own tag name. we mentioned them as `<TAG-NAME>` for the rest of this readme file.

> All fonts' formats is `.ttf`.

### Download Manually
See [releases](https://github.com/MohammadRaziei/fonts/releases)
to see all available fonts. then press on 
[<img alt="download" width="100em" src="https://github.com/MohammadRaziei/fonts/raw/master/readme/download-button.svg" style="margin-bottom:-.8em">](https://github.com/MohammadRaziei/fonts/releases)
button to download your specified font. Or you can manually download the `fonts.zip` file from the release's assets.

### Direct Link
 you can generate a direct link to the font in the following pattern. replace the `<TAG-NAME>` with the release name that you found at [releases](https://github.com/mohammadraziei/fonts/releases) page.

```bash
url="https://github.com/MohammadRaziei/fonts/releases/download/<TAG-NAME>/fonts.zip"
```

now you can download it using `curl` or `wget` commands.

```bash
# download with curl
curl -LO $url
# download with wget
wget $url
```




### Github actions

If you want to use them in github action you just need to know which `<TAG-NAME>` is suitable for your application. the following code download it into `fonts` directory in the root of the project and extract them automatically

```yaml
- name: Download Fonts
  uses: robinraju/release-downloader@v1.8
  with:
    ## Choose what fonts you need from
    # https://github.com/MohammadRaziei/fonts/releases
    tag: <TAG-NAME> # like "Latex-lite" 
    ####################################
    ## Do not change the following lines
    repository: "mohammadraziei/fonts"
    fileName: "fonts.zip"
    out-file-path: "fonts" # target folder
    extract: true
```

This option can help whenever you want to run a pipeline that needs to download some fonts. It can be widely used in compiling latex files in CI/CD workflows. 
As an example, you can see how this code helps in [our latex template](https://github.com/MohammadRaziei/latex-article-fa/blob/master/.github/workflows/build.yml).

---
:star: Hope that helps. Do not forget to star it. :dizzy: