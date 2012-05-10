# JRuby, Trinidad and Heroku

This is an example of a Rack application that can be deployed to Heroku on JRuby and Trinidad.

## Getting Started

To deploy this application you'll need to do the following:

    $ git clone git://github.com/jkutner/jruby-trinidad-heroku.git
    $ BUNDLE_GEMFILE=Jemfile bundle
    $ gem install heroku
    $ heroku create --stack cedar --buildpack http://github.com/heroku/heroku-buildpack-java
    $ git push heroku master

## Anatomy 

The most important parts of this project are:

*  pom.xml - this is a Maven config file that can be copied as is (in most cases).
*  Jemfile - a renamed Gemfile so that Heroku doesn't think this is an MRI app.
*  Procfile - a Heroku config file with instructions for running the app.
*  script/jruby - a modified jruby executable for the Heroku platform.
*  config.ru - the application itself (can be replaced with any Rack app)


