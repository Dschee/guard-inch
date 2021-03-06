# Guard::Inch

[![Inch CI](https://inch-ci.org/github/Chills42/guard-inch.svg?branch=master)](http://inch-ci.org/github/Chills42/guard-inch)
[![Code Climate](https://codeclimate.com/github/chills42/guard-inch/badges/gpa.svg)](https://codeclimate.com/github/chills42/guard-inch)

A Guard gem plugin that integrates the Inch documentation measurement tool. 

## Installation

Add this line to your application's Gemfile:

    gem 'guard-inch'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install guard-inch

## Usage

The plugin can be configured using `guard init inch`.

Afterward, just run guard

    guard

or

    bundle exec guard

and the tool will rerun `inch` on the files you are working with as you change them.

## Options

Other options can be set in the Guardfile

    guard :inch, pedantic: true, private: true, all_on_start: true, all_type: :stats do
      watch(/.+\.rb/)
    end

The above example shows use of several different options:

 - pedantic: determines whether or not to use the pedantic flag for changed file runs
 - private: as with `pedantic`, but for the private command-line flag
 - all_on_start: determines whether or not to do a `run all` on startup
 - all_type: specifies which run type should be used for `run all` with options mapping to those provided by inch

   - :stats
   - :list
   - :suggest

## Contributing

1. Fork it ( http://github.com/chills42/guard-inch/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
