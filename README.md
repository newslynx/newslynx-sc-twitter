[![Build status](https://travis-ci.org/newslynx/newslynx-sc-twitter.svg)](https://travis-ci.org/newslynx/newslynx-sc-twitter) [![Documentation Status](https://readthedocs.org/projects/newslynx-sc-twitter/badge/?version=latest)](https://readthedocs.org/projects/newslynx-sc-twitter/?badge=latest)
     

newslynx-sc-twitter
==========================================================================================

This module contains all Sous Chefs which deal with Twitter via \`twython\`.

## Installation

```bash
$ mkvirtualenv newslynx-sc-twitter
$ git clone https://github.com/newslynx/newslynx-sc-twitter.git
$ cd newslynx-sc-twitter
$ pip install .
```

## Tests

Requires `nose`

```bash
$ nosetests
```

## Documenation

Documentation for `newslynx-sc-twitter` is hosted on [Read The Docs](http://newslynx-sc-twitter.readthedocs.org/).

It's generated via the following steps

* converts this file (`README.md`) into a ReStructured Text file, saving it to [docs/index.rst](https://github.com/newslynx/newslynx-sc-twitter/blob/master/docs/index.rst)
* runs `newslynx sc-docs newslynx_sc_twitter -f rst` to generate documentation for all the Sous Chefs in `newslynx-sc-twitter` and saves the output to [docs/sous-chefs.rst](https://github.com/newslynx/newslynx-sc-twitter/blob/master/docs/sous-chefs.rst)
* Builds Sphinx Documentaiton from these files.


## Continuous Integration

Builds for `newslynx-sc-twitter` can be found on [Travis](https://travis-ci.org/newslynx/newslynx-sc-twitter)

## Contributing

See the [contributing guidelines](https://github.com/newslynx/newslynx-sc-twitter/blob/master/CONTRIBUTING.md).


## What's in this module ?

- [README.md](https://github.com/newslynx/newslynx-sc-twitter/blob/master/README.md)
	* This file 

- [VERSION](https://github.com/newslynx/newslynx-sc-twitter/blob/master/VERSION)
	* `newslynx-sc-twitter`'s source-of-truth version.

- [requirements.txt](https://github.com/newslynx/newslynx-sc-twitter/blob/master/requirements.txt)
	* `newslynx-sc-twitter`'s python dependencies.

- [MANIFEST.in](https://github.com/newslynx/newslynx-sc-twitter/blob/master/MANIFEST.in)
	* Specifications for which files to include in the PyPI distribution.
	* See the docs on this [here](https://docs.python.org/2/distutils/sourcedist.html#specifying-the-files-to-distribute).

- [setup.py](https://github.com/newslynx/newslynx-sc-twitter/blob/master/setup.py)
	* Specification's for building `newslynx-sc-twitter`'s PyPI dsitribution.

- [.travis.yml](https://github.com/newslynx/newslynx-sc-twitter/blob/master/.travis.yml)
	* Configurations for Travis Continuous Integration
	* You must activate this project on [travis-ci.org](https://github.com/newslynx/newslynx-sc-twitter/blob/master/http://travis-ci.org/) for this to run on subsequent updates.

- [Makefile](https://github.com/newslynx/newslynx-sc-twitter/blob/master/Makefile)
	* Helpers for managing `newslynx-sc-twitter`.
	* Includes:
		- `make clean`: 
			* Cleans out cruft from this directory.
		- `make install`: 
			* Installs `newslynx-sc-twitter`. Assumes that you're in a virtual environment.
		- `make all_tests`: 
			* Runs the tests.
		- `make readme`
			* Converts this file to `.rst`, including a table of contents, and saves it to [docs/index.rst](https://github.com/newslynx/newslynx-sc-twitter/blob/master/docs/index.rst)
		- `make sous_chef_docs`
			* Programmtically generates [Sous Chef documentation](https://github.com/newslynx/newslynx-sc-twitter/blob/master/docs/sous-chefs.rst) by running `newslynx sc-docs newslynx_sc_twitter/ --format=rst > docs/sous-chefs.rst`.
		- `make all_docs`: 
			* Builds the sphinx docs for `newslynx-sc-twitter` by running the above two commands.
		- `make view_docs`
			* Serves documentation at [localhost:8000](http://localhost:8000)
		- `make register`: 
			* Registers `newslynx-sc-twitter` on [PyPI](https://pypi.python.org/pypi).
		- `make distribute`: 
			* Publishes a new version of `newslynx-sc-twitter` to PyPI.

- [CONTRIBUTING.md](https://github.com/newslynx/newslynx-sc-twitter/blob/master/CONTRIBUTING.md)

- [newslynx_sc_twitter](https://github.com/newslynx/newslynx-sc-twitter/blob/master/newslynx_sc_twitter/)
	* `newslynx-sc-twitter`'s source code and Sous Chef configuration files.

- [docs](https://github.com/newslynx/newslynx-sc-twitter/blob/master/docs/)
	* Sphnix documentation for `newslynx-sc-twitter`

- [tests](https://github.com/newslynx/newslynx-sc-twitter/blob/master/tests/)
	* `nose` tests for `newslynx-sc-twitter`

