fake-airline-api
================

A simple application that fakes an airline's API.

The project uses:

* Flask - a python microframework - http://flask.pocoo.org/
* json - a python javascript object notation library
* sqlite3 - a python implementation of the sqlite database
* csv - python library for easy reading of delimited flat files

## Quick start.

###Required tools:

* [Python](https://www.python.org/downloads/)
* [Virtualenv](http://virtualenv.readthedocs.org/en/latest/)
 
####Quickstart for virtualenv
		easy_install pip
		pip install virtualenv

### Get the Project
1. Clone the project somewhere and go into the directory

		git clone https://github.com/TransactCharlie/fake-airline-api.git
		cd fake-airline-api


2. Build a new virtualenv
 
	`virtualenv env --no-site-packages`

3. source virtualenv:

	On Linux

		source env/bin/activate


	On Windows

		env\Scripts\activate

4. install dependencies

	`pip install -r requirements.txt`

5. initialise sql lite db

	`python data_loader.py`

6. run the API.

	`python fake_airline_api.py`

## Test Call
open a browser and connect to: [http://localhost:5000/all_routes](http://localhost:5000/all_routes)

You should get back a json object that looks like:

```json
[
  {
    "Price": 100,
    "ToIATA": "LHR",
    "ReturnDate": "2014-04-07",
    "DepartureDate": "2014-04-01",
    "FromIATA": "EDI"
  },
  {
    "Price": 5000,
    "ToIATA": "EWR",
    "ReturnDate": "2014-08-12",
    "DepartureDate": "2014-08-04",
    "FromIATA": "GLA"
  }
]
```

## api documentation

**TODO!**

call: [http://localhost:5000/api/EDI/LHR/2014-04-01/2014-04-07](http://localhost:5000/api/EDI/LHR/2014-04-01/2014-04-07)

Response:

```json
[
  {
    "Price": 100,
    "ToIATA": "LHR",
    "ReturnDate": "2014-04-07",
    "DepartureDate": "2014-04-01",
    "FromIATA": "EDI"
  }
]```