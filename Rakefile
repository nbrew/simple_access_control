require 'rubygems'
require 'rake'
require 'rake/testtask'
require 'rake/rdoctask'


begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "nbrew-simple_access_control"
    gem.summary = %Q{Simple role-based access control plugin for Rails controllers and views.}
    gem.description = %Q{Simple access controls for use with ActsAsAuthenticated, RestfulAuthentication, etc. A clone of Mathew Abonyi's (mabs29) repo: http://mabs29.googlecode.com/svn/trunk/plugins/simple_access_control}
    gem.email = "nhyde@bigdrift.com"
    gem.homepage = "http://github.com/nbrew/simple_access_control"
    gem.authors = ["Mathew Abonyi"]
    gem.add_development_dependency "shoulda", ">= 0"
    # gem is a Gem::Specification... see http://www.rubygems.org/read/chapter/20 for additional settings
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: gem install jeweler"
end


desc 'Default: run unit tests.'
task :test => :check_dependencies
task :default => :test

desc 'Test the simple_access_control plugin.'
Rake::TestTask.new(:test) do |t|
  t.libs << 'lib'
  t.pattern = 'test/**/*_test.rb'
  t.verbose = true
end

desc 'Generate documentation for the simple_access_control plugin.'
Rake::RDocTask.new(:rdoc) do |rdoc|
  rdoc.rdoc_dir = 'rdoc'
  rdoc.title    = 'SimpleAccessControl'
  rdoc.options << '--line-numbers' << '--inline-source'
  rdoc.rdoc_files.include('README')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
