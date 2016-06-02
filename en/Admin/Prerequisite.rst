Prerequisite
============

Phraseanet is supposed to work on an AMP system, which configuration has to
be checked.

HTTP Server
------------

One of these

* Nginx >= 1.0 (Recommanded) -- :doc:`configuration <Configuration/Nginx>`
* or Apache >= 2.2 -- :doc:`configuration <Configuration/Apache>`

Database
--------

Phraseanet requires an InnoDB storage engine. MySQL, MariaDB or Percona can be
used for this.

* MySQL >= 5.5

PHP
---

* Phraseanet requires PHP version 5.5.0 (or greater) with the following
  extensions:

    * Dom
    * exif
    * ftp
    * gd2
    * hash
    * iconv
    * xml
    * mbstring
    * mysql
    * pcre
    * pcntl (unix)
    * SimpleXML
    * sockets
    * xsl +zlib
    * mcrypt
    * twig (https://github.com/fabpot/Twig/tree/master/ext/)
    * intl
    * pdo
    * CURL
    * JSON
    * gettext
    * amqp

.. _Installer-Elasticsearch:

Elasticsearch
-------------

Phraseanet 4.0 builds on the ElasticSearch engine with the following
specifications:

    * Version 1.7 à 2.0
    * `Analysis-icu`_ plugin corresponding to the used Elasticsearcher engine release

Locales
-------

On Unix / GNU-Linux systems, it is necessary to enable locales to use
Phraseanet in your languages.

Debian example:

.. code-block:: bash

    dpkg-reconfigure locales

Ubuntu example:

* Activate via /etc/locale.gen
* Execute /usr/sbin/locale-gen

.. note::

    Locales must be in UTF-8.

Third Party Programs
--------------------

To generate subviews, Phraseanet uses third party programs, depending
on their type

* Ufraw
  ImageMagick deleagtion for RAW images

* FFmpeg from version 1.2.12 "Magic" to 2.0.7 "Nameless" (Tested versions)
  Previews and Thumbnails extraction from videos and audios.

  .. note::

      Add codecs:

* Ghostscript
  Previews and thumbnails extraction from graphix vectors and postscript.

* XPDF
  Text extraction from PDFs.

* SWFTools
  Previews and thumbnails extraction from Adobe Flash files.

* Exiftool
  RDF metadatas extraction.

* Unoconv >= 6
  Preview and thumbnails extraction from office documents.

* MP4Box
  Preview extraction from videos.

API keys (optional)
--------------------

* Youtube
* Dailymotion
* FlickR
* Recpatcha

.. _Analysis-icu: https://github.com/elastic/elasticsearch-analysis-icu
