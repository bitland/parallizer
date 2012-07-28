require 'rubygems'
require 'bundler'
begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = "parallizer"
  gem.homepage = "http://github.com/michaelgpearce/parallizer"
  gem.license = "MIT"
  gem.summary = %Q{Execute your service layer in parallel.}
  gem.description = %Q{Execute your service layer in parallel.}
  gem.email = "michael.pearce@bookrenter.com"
  gem.authors = ["Michael Pearce"]
  # Include your dependencies below. Runtime dependencies are required when using your gem,
  # and development dependencies are only needed for development (ie running rake tasks, tests, etc)
  gem.add_runtime_dependency 'work_queue', '>= 0'
  gem.add_development_dependency 'shoulda', '>= 0'
end
Jeweler::RubygemsDotOrgTasks.new

require 'rake/testtask'
Rake::TestTask.new(:test) do |test|
  test.libs << 'lib' << 'test'
  test.pattern = 'test/**/*_test.rb'
  test.verbose = true
end

task :default => :test
