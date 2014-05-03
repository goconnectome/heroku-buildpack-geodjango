# Heroku buildpack: Python and geoip, geos, proj4, gdal

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for Python apps, powered by [pip](http://www.pip-installer.org/).


## Usage

Example usage:

    $ ls
    Procfile  requirements.txt  web.py

    $ heroku create --buildpack git://github.com/OShalakhin/heroku-buildpack-geodjango

    $ git push heroku master

You can also add it to upcoming builds of an existing application:

    $ heroku config:add BUILDPACK_URL=git://github.com/heroku/heroku-buildpack-python.git

The buildpack will detect your app as Python if it has the file `requirements.txt` in the root.

It will use Pip to install your dependencies, vendoring a copy of the Python runtime into your slug.

## Specify a Runtime

You can also provide arbitrary releases Python with a `runtime.txt` file.

    $ cat runtime.txt
    python-3.3.3

Runtime options include:

- python-2.7.6
- python-3.3.3
- pypy-1.9 (experimental)

Other [unsupported runtimes](https://github.com/kennethreitz/python-versions/tree/master/formula) are available as well.
