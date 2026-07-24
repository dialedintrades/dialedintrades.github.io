source "https://rubygems.org"

gem "json", "2.19.1"
gem "jekyll", "~> 4.3"

# Pin to the libsass-based converter (no Sass in this project) to avoid
# jekyll-sass-converter 3.x's sass-embedded -> google-protobuf -> bigdecimal
# chain, whose native extension fails to build on several toolchains.
gem "jekyll-sass-converter", "~> 2.2"

group :jekyll_plugins do
  gem "jekyll-feed"
  gem "jekyll-sitemap"
  gem "jekyll-seo-tag"
end

gem "webrick", "~> 1.8"
