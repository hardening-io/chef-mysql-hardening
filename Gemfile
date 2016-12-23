# encoding: utf-8

source 'https://rubygems.org'

gem 'berkshelf', '~> 5.3'
gem 'chef', '~> 12.5'

# pin dependency for Ruby 1.9.3 since bundler is not
# detecting that net-ssh 3 does not work with 1.9.3
if Gem::Version.new(RUBY_VERSION) <= Gem::Version.new('1.9.3')
  gem 'net-ssh', '~> 2.9'
end

group :test do
  gem 'rake'
  gem 'chefspec',   '~> 4.2.0'
  gem 'foodcritic', '~> 4.0'
  gem 'rubocop', '~> 0.46.0'
  gem 'coveralls',  require: false
  gem 'bundler', '~> 1.5'
  gem 'minitest', '~> 5.5'
  gem 'simplecov', '~> 0.10'
end

group :development do
  gem 'guard'
  gem 'guard-rspec'
  gem 'guard-kitchen'
  gem 'guard-rubocop'
  gem 'guard-foodcritic'
end

group :integration do
  gem 'test-kitchen', '~> 1.0'
  gem 'kitchen-vagrant'
  gem 'kitchen-dokken'
  gem 'kitchen-inspec', '~> 0.9'
  gem 'concurrent-ruby', '~> 0.9'
end

group :tools do
  gem 'github_changelog_generator', '~> 1.12.0'
end
