begin
  require 'bundler/setup'
rescue LoadError
  puts 'You must `gem install bundler` and `bundle install` to run rake tasks'
end

require 'rdoc/task'
require 'rspec/core/rake_task'

RSpec::Core::RakeTask.new(:spec)

RDoc::Task.new(:rdoc) do |rdoc|
  rdoc.rdoc_dir = 'rdoc'
  rdoc.title    = 'WebpackRails'
  rdoc.options << '--line-numbers'
  rdoc.rdoc_files.include('README.rdoc')
  rdoc.rdoc_files.include('lib/**/*.rb')
end

Bundler::GemHelper.install_tasks

task default: :spec
