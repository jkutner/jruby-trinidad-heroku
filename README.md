# JRuby, Trinidad and Heroku

This is an example of a Rack application that can be deployed to Heroku on JRuby and Trinidad.

## Getting Started

To deploy this application you'll need to do the following:

    $ git clone git://github.com/jkutner/jruby-trinidad-heroku.git
    $ BUNDLER_GEMFILE=Jemfile bundle
    $ gem install heroku
    $ heroku create --stack cedar --buildpack http://github.com/heroku/heroku-buildpack-java
    $ git push heroku master

