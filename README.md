# Heroku CORS proxy

[![Greenkeeper badge](https://badges.greenkeeper.io/Alorel/heroku-cors-proxy.svg)](https://greenkeeper.io/)
![Node Version Support: 7.6+](https://img.shields.io/badge/Node%20Version%20Support-7.6%2B-brightgreen.svg)
[![Build Status](https://travis-ci.org/Alorel/heroku-cors-proxy.svg?branch=master)](https://travis-ci.org/Alorel/heroku-cors-proxy)

[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.png)](https://www.heroku.com/deploy/?template=https://github.com/Alorel/heroku-cors-proxy)

A CORS-enabled Express proxy server ready to deploy to Heroku.

# Features

* Origin whitelisting
* Caching
* Automatic minification of HTML and JSON responses
* Automatic brotli and/or gzip compression

# Restrictions

* Only GET requests are permitted
* Requests without an origin header are rejected

# Configuration

All configuration is done via environment variables

## ORIGIN_WHITELIST

A comma-separated list of domain names allowed to use the proxy.

For example, if you want the proxy to be accessible from `www.foo.com`
and `foo.com` you can set this to `www.foo.com,foo.com`.

Leave empty to allow all origins.

## TARGET_WHITELIST

Same as `ORIGIN_WHITELIST`, but for the domain names of URLs we're
CORSing.

## CACHE_TIME

Amount of time, in milliseconds, that cacheable responses will be stored in Redis. Omit or set to 0 to disable caching.

## LOG_LEVEL

Logging level. Permitted values, in order of priority:

* emerg
* alert
* crit
* error
* warning
* notice
* info
* debug

# Supported versions

7.6+
