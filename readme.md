# USGS Data Tools

A python package to assist with data management best practices.

##### USGS Digital Object Identifer Tool (internal tool)

This module supports a python wrapper ontop of the usgs doi tool. 

✅ User sessions

✅ Creating digital object identifiers

✅ Update digital object identifiers

✅ Query the tool

##### Datacite 

Convienience function to query a DOI that's in DataCite to return attributes.

✅ Query DOI 

##### Metadata Parser 

✅ Validate local files (XML)

### Quick Start

```python
from usgs_datatools import doi

doi_session = doi.DoiSession()
doi_session.doi_authenticate("someperson@usgs.gov", "somepassword")

# Get DOI
my_doi = doi_session.get_doi("doi:10.5066/xxxx")

# Create DOI
doi_session.doi_create({'title': 'USGS Datatools Test Creation',
                        'datasource_id': '17501', 
            		   'status': 'reserved'})
```

### Install 

The preferred method for installation is using the latest version release here on github.

```sh
pip install git+https://github.com/bserna-usgs/usgs_datatools.git
```

__Local files__

If you are working with a downloaded copy of this package here's some helpful steps

Install python requirements (using pipenv)

```
pipenv install
```

I will periodically update the requirements.txt file as well

```
pip install -r requirements.txt
```

### Examples

Please see the examples/notebook directory for a sample of DOI Tool usage (querying, creating, modifying).

Datacite queries can be ran using the new ```doi.datacite_search(10.5066/xxxxx)``` method.

### Contributions

All kinds of contibutions are greatly appreicated, please see the ```CONTRIBUTING.rst``` file for more information [link](https://github.com/bserna-usgs/usgs_datatools/blob/master/CONTRIBUTING.rst)


### Testing

Testing is setup using pytest and can be started using the command below.

```sh
python -m pytest tests/
```

### Development

Update versions

```sh
# preferred and w/o commit 
bumpversion minor

# old
bumpversion  --current-version 0.2.0 minor --allow-dirty
```

### Documentation

Go into the docs folder and build

```
make html
```

<hr>

### Provisional Software Disclaimer Under USGS Software Release Policy, the software codes here are considered preliminary, not released officially, and posted to this repo for informal sharing among colleagues.

This software is preliminary or provisional and is subject to revision. It is being provided to meet the need for timely best science. The software has not received final approval by the U.S. Geological Survey (USGS). No warranty, expressed or implied, is made by the USGS or the U.S. Government as to the functionality of the software and related material nor shall the fact of release constitute any such warranty. The software is provided on the condition that neither the USGS nor the U.S. Government shall be held liable for any damages resulting from the authorized or unauthorized use of the software.
