# Web Operations Conferences

_Notice_: I am no longer maintaining this site.

[![Build Status](https://travis-ci.org/webopsconferences/webopsconferences.github.io.svg?branch=master)](https://travis-ci.org/webopsconferences/webopsconferences.github.io)

This is the source to the now-defunct [www.webopsconferences.com](http://www.webopsconferences.com). The purpose of the site aws to list conferences of interest to people working in the field of [web operations](http://omniti.com/seeds/what-is-web-operations).

## Building

All the data on conferences is stored in `conferences.yml`,  so to add a new one or update an existing one all you have to do is edit that. I hope the structure is self-explanatory, but if not just ask.

The conference data is combined with the template in `index.html.erb` to create the site's contents. The build process is defined in the `Rakefile`.

If you have a working ruby environment, you can install the dependencies and build the site with

    bundle install
    bundle exec rake
