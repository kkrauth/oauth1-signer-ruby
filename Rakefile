require 'rubygems'
require 'rake'
require 'rake/clean'
require 'rake/testtask'

Rake::TestTask.new do |t|
  t.libs << "tests"
  t.test_files = FileList['tests/*test*.rb']
  t.verbose = true
end

Dir['tasks/**/*.rake'].each { |t| load t }

desc "Run tests"
task :default => :test