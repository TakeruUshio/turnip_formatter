RSpec::Core::Formatters::TurnipFormatter
========================================

TurnipFormatter is a pretty custom formatter for [Turnip](https://github.com/jnicklas/turnip).

[![Build Status](https://travis-ci.org/gongo/turnip_formatter.png?branch=master)](https://travis-ci.org/gongo/turnip_formatter)
[![Coverage Status](https://coveralls.io/repos/gongo/turnip_formatter/badge.png?branch=master)](https://coveralls.io/r/gongo/turnip_formatter)
[![Code Climate](https://codeclimate.com/github/gongo/turnip_formatter.png)](https://codeclimate.com/github/gongo/turnip_formatter)
[![Dependency Status](https://gemnasium.com/gongo/turnip_formatter.png)](https://gemnasium.com/gongo/turnip_formatter)

Requirements
--------------------

* Ruby
    * `~> 1.9.3`
    * `~> 2.0.0`

Installation
--------------------

### RubyGems

    $ gem install turnip_formatter

### Bundler

Add this line to your application's Gemfile:

```ruby
group :test do
  gem 'turnip_formatter'
end
```

And then execute:

    $ bundle install

Usage
--------------------

Run this command.

    $ rspec -r turnip_formatter --format RSpecTurnipFormatter --out report.html


Screenshot
--------------------

### Step overview

![Tab steps](https://github.com/gongo/turnip_formatter/raw/master/images/tab_steps.png)

expand:

![Expand tab steps](https://github.com/gongo/turnip_formatter/raw/master/images/tab_steps_expanding.png)

### Speed Statistics

![Expand tab steps](https://github.com/gongo/turnip_formatter/raw/master/images/tab_speed_statistics.png)

### Feature Statistics

![Expand tab steps](https://github.com/gongo/turnip_formatter/raw/master/images/tab_feature_statistics.png)

### Tag Statistics

![Expand tab steps](https://github.com/gongo/turnip_formatter/raw/master/images/tab_tag_statistics.png)


Example
--------------------

See:

- Feature and Steps
    - https://github.com/gongo/turnip_formatter/tree/master/example
- Report
    - http://gongo.github.io/turnip_formatter/examples/report.html

Configuration
--------------------

```ruby
TurnipFormatter.configure do |config|
  config.title = 'My Report'                                 # <h1>My Report</h1>
  config.add_stylesheet File.dirname(__FILE__) + '/foo.css'  # <style>..</style>
  config.add_javascript File.dirname(__FILE__) + '/bar.js'   # <script>..</script>

  config.add_stylesheet 'http://cdn.example.com/hoge.css'    # <link rel="..">
  config.add_javascript '//cdn.example.com/fuga.js'          # <script src="..">
end
```

Add-on
--------------------

* Gnawrnip
    * Gnawrnip is a TurnipFormatter Add-on that provides put a screen shot to report use Capybara
    * https://github.com/gongo/gnawrnip

License
--------------------

see LICENSE.txt
