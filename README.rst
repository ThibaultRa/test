======
LSC - Scrapy
======

Goal
========

This project aims at building a generic crawling/scraping solution which would
gather a maximum of relevant information without the need of extensive
computation power. Indeed the tailored crawlers used at the time of this project
development were missing informations such as quarterly reports, presentations…
Such technology will eventually help Spinergie to have a huge energy database
associated with a search engine plugged upon.

This project is build on Scrapy. It is a fast high-level web crawling and web
scraping framework, used to crawl websites and extract structured data from
their pages. It can be used for a wide range of purposes, from data mining to
monitoring and automated testing.

For more information including a list of features check the Scrapy homepage at:
https://scrapy.org

.. figure::  https://static.wixstatic.com/media/7e5ca4_e8c5873752d243559bf196835cd1924b~mv2.png/v1/fill/w_154,h_85,al_c,usm_0.66_1.00_0.01/7e5ca4_e8c5873752d243559bf196835cd1924b~mv2.png
   :align:  center

Requirements
============

* Python 2.7
* Works on Linux and Mac OSX
* tldextract 2.2.0
* tika 1.15
* pandas 0.20.3
* python-pptx 0.6.5
* xlrd 1.0.0
* pymongo 3.5.1
* scrapy 1.4.0
* Twisted 17.9.0
* Pillow 4.1.1
* w3lib 1.18.0
* numpy 1.13.3
* six 1.11.0
* lxml 4.1.0
* fake-useragent 0.1.8
* slacker 0.9.60
* PyMySQL 0.7.11
* bs4 0.0.1
* requests 2.18.4
* python-Levenshtein 0.12.0
* email 4.0.2
* python-magic 0.4.15

Basic Commands
=======

It is assumed that the following commands are executed with
``Crawling_largescale`` set as the current working directory.

Launch a crawl
----------------

The following command

    python run.py 1 2

will launch a crawl on websites whose id are 1 & 2 in the lsc_websites sql table
on Rig Master.

Output KPIs
----------------

The following command

    python kpis.py 30 statoil.com seadrill.com

will produce kpis on every document in the MongoDB database that stems from a
starting url whose domain is either statoil.com or seadrill.com. The crawling
rate will be displayed as:

$$\\frac{ number of documents modified in db }{30 minutes}$$

Documentation
=============

Documentation is available in the ``documentation`` directory.
