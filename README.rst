OVAL --- BASE OAI-PMH Validity Checker
======================================

Package for testing OAI-PMH interfaces' compliance with the requirements of
the BASE search engine (http://base-search.net/). This package powers the Web application
located at http://oval.base-search.net/.

Dependencies
------------

* ordereddict
* argparse
* lxml

Installation
------------

Use ``setup.py``::

   python setup.py build
   sudo python setup.py install

Basic Usage
-----------
  >>> from oval.validator import Validator
  >>> validator = Validator('http://eprints.rclis.org/dspace-oai/request')
  
  >>> validator.repository_name
  u'E-LIS. E-prints in Library and Information Science'
  
  >>> validator.admin_email
  u'elis@cilea.it'
  
  >>> validator.validate_XML('ListRecords')
  >>> validator.results['ListRecordsXML']
  ('ok', 'ListRecords response well-formed and valid.')