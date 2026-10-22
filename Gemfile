source "https://rubygems.org"
# Hello! This is where you manage which Jekyll version is used to run.
# When you want to use a different version, change it below, save the
# file and run `bundle install`. Run Jekyll with `bundle exec`, like so:
#
#     bundle exec jekyll serve
#
# This will help ensure the proper Jekyll version is running.
# Happy Jekylling!
#
# The site is built by GitHub Pages, so we use the same gem (and Jekyll version)
# it uses. To upgrade, run `bundle update github-pages`.
# The theme (minima) and plugins (jekyll-feed, jekyll-seo-tag) come with it.
gem "github-pages", group: :jekyll_plugins
# Gems no longer bundled with recent Rubies but needed by Jekyll 3.x
gem "base64"
gem "bigdecimal"
gem "csv"
gem "logger"
gem "ostruct"

# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", "~> 1.2"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]

gem "webrick", "~> 1.8"
