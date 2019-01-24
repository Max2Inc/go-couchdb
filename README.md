# VEEA Systems

This is a fork of https://vsys/go-couchdb.

The original project does not support CouchDB 2.x and it
appears to have been abandoned - a PR fixing the CouchDB
2.x compatibility has been open for more than two years.

If the upstream maintainer ever merges the PR, this repo
can be deleted and we can return to using the upstream
repository directly.

# What's this?

go-couchdb is yet another CouchDB client written in Go.
It was written because all the other ones didn't provide
functionality that I need.

The API is not fully baked at this time and may change.

This project contains three Go packages:

## package couchdb [![GoDoc](https://godoc.org/vsys/go-couchdb?status.png)](http://godoc.org/vsys/go-couchdb)

    import "vsys/go-couchdb"

This wraps the CouchDB HTTP API.

## package couchapp [![GoDoc](https://godoc.org/vsys/go-couchdb?status.png)](http://godoc.org/vsys/go-couchdb/couchapp)

    import "vsys/go-couchdb/couchapp"

This provides functionality similar to the original
[couchapp](https://github.com/couchapp/couchapp) tool,
namely compiling a filesystem directory into a JSON object
and storing the object as a CouchDB design document.

## package couchdaemon [![GoDoc](https://godoc.org/vsys/go-couchdb?status.png)](http://godoc.org/vsys/go-couchdb/couchdaemon)

    import "vsys/go-couchdb/couchdaemon"

This package contains some functions that help
you write Go programs that run as a daemon started by CouchDB,
e.g. fetching values from the CouchDB config.

# Tests

You can run the unit tests with `go test`.

[![Build Status](https://travis-ci.org/fjl/go-couchdb.png?branch=master)](https://travis-ci.org/fjl/go-couchdb)
