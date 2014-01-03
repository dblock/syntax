require 'bundler/setup'
require 'rake/testtask'
require 'bundler/gem_tasks'

Rake::TestTask.new :default do |t|
  t.test_files = [ "test/ALL-TESTS.rb" ]
  t.verbose = true
end

desc "Generate the manual"
task :manual => [ "doc/manual-html/index.html" ]

file "doc/manual-html/index.html" => [ "doc/manual/manual.yml" ] do
  cd( "doc/manual" ) { ruby "manual.rb ../manual-html" }
end
