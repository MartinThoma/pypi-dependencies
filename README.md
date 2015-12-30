# Python Package dependencies 
## About
This package contains a JSON file which represents the dependency graph of 
Python packages.

The JSON file is a dictionary with three keys:

* meta: Some meta information like from which time the data is and
        the version of the software which is used to scrape/analyze the data
* packages: A list of dictionaries. Each dictionary represents a package and
  has the keys
  * 'id' (int, internal number),
  * 'name' (str, name on PyPI)
* dependencies: A list of dictionaries. Each dictionary represents a
  dependency and has the keys
  * `pkg`: ID of the package which has a dependency
  * `needs_pkg`: ID of the package which is being imported / required
  * `type`: The type of dependency (e.g. 'import', 'requirements.txt', ...)
  * `times`: int
      Only makes sense with `'type': 'import'`. It means how often a package
      was imported.

## License
This work is licensed unter the MIT License. See the [LICENSE file](LICENSE)
