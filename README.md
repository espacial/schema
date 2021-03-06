DataCite Schema Repository
==========================

[![Build Status](https://travis-ci.org/datacite/schema.svg?branch=labs)](https://travis-ci.org/datacite/schema)

This repository holds the official metadata schemas from DataCite as
required by the DataCite Metadata Store.

It contains the schemas itself along with examples and documentation.
There is also a small maven project to test the schemas for consistency.

If you have any comments or questions regarding the schema please post them in our Google Group:
https://groups.google.com/forum/?hl=en&fromgroups#!forum/datacite-metadata

Schemas
-------

Each schema has its own folder under `/meta`
e.g. `/meta/kernel-2.0/`. This directory is allowed to contain
only one xsd. The directory structure is as follow:

    /meta/{schema-name}/{filename}.xsd   root xsd
    /meta/{schema-name}/include/         referenced xsd's
    /meta/{schema-name}/example/         example xml files
    /meta/{schema-name}/doc/             documentation (pdf's)

The `/metat` directory will be published at http://schema.datacite.org, e.g.

    http://schema.datacite.org/meta/kernel-2.0/metadata.xsd

Tests
-----

There are tests to check the directory structure, existence of examples,
validity of the schemas, and validity of the examples.

You can execute the tests via

    mvn test
