require 'echoe'
Echoe.new('torrent_api', '0.2.8') do |p|
  p.description = "An API to query popular torrent websites"
  p.url = "http://www.github.com/hjhart/torrent_api"
  p.author = "James Hart"
  p.email = "hjhart@gmail.com"
  p.ignore_pattern = ["tmp/**/*", "scripts/*", "spec/**/*", "Gemfile*"]
  p.runtime_dependencies = ['nokogiri', 'hpricot']
end

task :default => :console

task :console do
  sh "irb -rubygems -r ./lib/torrent_api.rb"
end

begin
  require 'rspec/core/rake_task'
  RSpec::Core::RakeTask.new(:spec)
rescue LoadError
end
