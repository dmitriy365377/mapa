# Karte von morgen

![Screenshot](https://raw.githubusercontent.com/flosse/kartevonmorgen/master/screenshot.jpg)

## Mapping for Good

von morgen supports kindness, sustainability and joint action.
Everything that brings a little happiness to our world.
We believe that living in a de‐stressed, environmental‐friendly and
trust‐worthy society, is already in progress.
We want to support people in finding ways to embrace those values.

The Map von morgen is a website and app, that allows users to share their
favorite places in the world. Places that are forward‐thinking and inspiring.
The goal is to collect projects, companies and events that make a world of
tomorrow, already experienceable today.

Demo: [https://kartevonmorgen.org/](https://kartevonmorgen.org/)

## Development

[![Build Status](https://secure.travis-ci.org/flosse/kartevonmorgen.svg?branch=master)](http://travis-ci.org/flosse/kartevonmorgen)
[![Dependency Status](https://gemnasium.com/flosse/kartevonmorgen.svg)](https://gemnasium.com/flosse/kartevonmorgen)
[![Dependency Status](https://dependencyci.com/github/flosse/kartevonmorgen/badge)](https://dependencyci.com/github/flosse/kartevonmorgen)
[![License](https://img.shields.io/badge/license-AGPLv3-blue.svg?style=flat)](https://github.com/flosse/kartevonmorgen/blob/master/LICENSE)

Are you're interested in contributing to KVM?
The following is a description of a quickstart.
If you're looking for a more comprehensive introduction,
have a look at [CONTRIBUTING.md](CONTRIBUTING.md).

### Dependencies

To be able to start development you'll need the following tools:

- [git](https://www.git-scm.com/)
- [Node.js](https://nodejs.org/) version 6.x
- [npm](https://www.npmjs.com/package/npm) version 3.x or [Yarn](https://yarnpkg.com/en/docs/getting-started)
- [OpenFairDB](https://github.com/slowtec/openfairdb)

Now clone this repository:

    git clone https://github.com/diglabby/mapa

Go to the root of it and install all the dependencies:

    cd goodmap-old/
    npm install
or 
    yarn
    
### Local development setup

The easiest way to get a local setup running is by using the remote API of [OpenFairDB](https://github.com/slowtec/openfairdb).
To do so change `src/constants/URLs.js` to
https://github.com/goodmap/goodmap-old/blob/e9658f1d2a8d77effe4cfabc085b5c7a2c65c3f3/src/constants/URLs.js#L64

``` js
OFDB_API: {
  //link: window.location.origin + "/api" //use when you run openfairdb locally
  link: window.location.protocol + "//" + "api.ofdb.io/v0" //use this to use the remote api
}
```

The alternative is to run OpenFairDB Server locally:

####Linux setup:

``` sh
wget https://download.ofdb.io/openfairdb-x86_64-linux-v0.3.1.tar.gz
tar xzf openfairdb-x86_64-linux-v0.3.1.tar.gz
./openfairdb
```
`openfairdb` should now be listening on port 6767.

To actually get started you also need to add some [content](https://github.com/flosse/openfairdb/files/2511314/openfair.db.zip). (Save database, copy it to local repository, unzip and override the previous database).

####Docker setup:

1. Clone the [openfairdb](https://github.com/slowtec/openfairdb) repo.
2. Go to `openfairdb` folder: `cd ./openfairdb`
3. Build image and run the container by commands from [openfairdb](https://github.com/slowtec/openfairdb#docker) repo
4. `openfairdb` should now be listening on port 6767.

Get the web app running:

``` sh
    cd /path/to/goodmap-old/
    npm start
```
or 
```
    yarn start
```

The web app is now listening on port 8080.
Open it in your browser `https://localhost:8080`.

On every file change in `src/`, the app will be build
for you and the browser reloads automatically.

### Tests

All the tests can be found in the `spec/` folder.
To run the tests type

    npm t

### Backend

KVM uses the [OpenFairDB](https://github.com/slowtec/openfairdb) as its backend.

## Goodmap
<3 Goodmap Consortium

### Core
* Navigate to `goodmap-core` folder
* Add changes
* Recompile by using `yarn build`

### Webapp
* Navigate to `goodmap-webapp` folder
* Install via `yarn install`
* Add changes
* Run by using `yarn start`

## License

Copyright (c) 2015 - 2018 Markus Kohlhase <mail@markus-kohlhase.de>

This project is licensed under the [AGPLv3 license](http://www.gnu.org/licenses/agpl-3.0.txt).
