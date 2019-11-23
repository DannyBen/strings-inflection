<div align="center">
  <img width="225" src="https://github.com/piotrmurach/strings/blob/master/assets/strings_logo.png" alt="strings logo" />
</div>

# Strings::Inflect

[![Gem Version](https://badge.fury.io/rb/strings-inflect.svg)][gem]
[![Build Status](https://secure.travis-ci.org/piotrmurach/strings-inflect.svg?branch=master)][travis]
[![Build status](https://ci.appveyor.com/api/projects/status/v8beeg5pmsdncvu8?svg=true)][appveyor]
[![Maintainability](https://api.codeclimate.com/v1/badges/4951f64ee240909fbde1/maintainability)][codeclimate]
[![Coverage Status](https://coveralls.io/repos/github/piotrmurach/strings-inflect/badge.svg?branch=master)][coverage]
[![Inline docs](http://inch-ci.org/github/piotrmurach/strings-inflect.svg?branch=master)][inchpages]

[gem]: http://badge.fury.io/rb/strings-inflect
[travis]: http://travis-ci.org/piotrmurach/strings-inflect
[appveyor]: https://ci.appveyor.com/project/piotrmurach/strings-inflect
[codeclimate]: https://codeclimate.com/github/piotrmurach/strings-inflect/maintainability
[coverage]: https://coveralls.io/github/piotrmurach/strings-inflect?branch=master
[inchpages]: http://inch-ci.org/github/piotrmurach/strings-inflect

> Convert between singular and plural forms of English nouns.

**Strings::Inflect** provides noun conversions to singular and plural form component for [Strings](https://github.com/piotrmurach/strings).

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'strings-inflect'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install strings-inflect

## Contents

* [1. Usage](#1-usage)
* [2. API](#2-api)
  * [2.1 inflect](#21-inflect)
  * [2.2 singularize](#22-singularize)
  * [2.3 pluralize](#23-pluralize)
  * [2.4 join_words](#24-join-words)

## 1. Usage

**Strings::Inflect** provides `pluralize` to convert a noun to plural form:

```ruby
Strings::Inflect.pluralize("error")
# => "errors"
```

To inflect a noun to a singular form use `singularize` method:

```ruby
Strings::Inflect.singularize("errors")
# => "error"
```

There is also more generic `inflect` method that accepts a noun and count:

```ruby
Strings::Inflect.inflect("error", 3)
# => "errors"
```

## 2. API

### 2.1 inflect

### 2.2 singularize

### 2.3 pluralize

### 2.4 join_words

To join an array of words into a single sentence use `join_words` method.

For example, to join three words:

```ruby
Strings::Inflect.join_words("one", "two", "three")
# => "one, two, and three"
```

To join words without Oxford style comma use `:final_separator`:

```ruby
Strings::Inflect.join_words("one", "two", "three", final_separator: "")
# => "one, two and three"
```

To join words with custom separators:

```ruby
options = {
  separator: " or ",
  final_separator: " or at least ",
  conjunctive: ""
}
Strings::Inflect.join_words("one", "two", "three", **options)
# => "one or two or at least three"
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/piotrmurach/strings-inflect. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

## Code of Conduct

Everyone interacting in the Strings::Inflect project’s codebases, issue trackers, chat rooms and mailing lists is expected to follow the [code of conduct](https://github.com/[USERNAME]/strings-inflect/blob/master/CODE_OF_CONDUCT.md).


## Copyright

Copyright (c) 2019 Piotr Murach. See LICENSE for further details.
