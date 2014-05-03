# Heroku Buildpack for Python/Django with geoip, gdal, proj4, geos

## Usage

With heroku:

```bash
heroku create --buildpack https://github.com/OShalakhin/heroku-buildpack-geodjango
```

With dokku add the following line to `.env`:

```bash
export BUILDPACK_URL=https://github.com/OShalakhin/heroku-buildpack-geodjango
```

and in the end:

```bash
# for heroku
git push heroku master
# for dokku
git push production master
```

