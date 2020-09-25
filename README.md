# Hugo Docker Builder

This fork is for automaticaly building docker images for `hugo`.

If you are interested in the upstream project please refer to [gohugoio/hugo](https://github.com/gohugoio/hugo).

## Docker Images

Images are available here: [deluca/hugo](https://hub.docker.com/r/deluca/hugo).  
*Most buildable tags have been built and are pushed to the repository.*

## Usage

Example from the [official quick-start page](https://gohugo.io/getting-started/quick-start/).

**Create a site**
```shell script
docker run -it --rm -v ${PWD}:/site deluca/hugo:latest new site quickstart
```

**Add a theme**
```shell script
cd quickstart
git init
git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke
echo 'theme = "ananke"' >> config.toml
```

**Start the server**
```shell script
docker run -it --rm -v ${PWD}:/site -p 1313:1313 deluca/hugo:latest server -D --bind 0.0.0.0
```
