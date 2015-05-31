require 'rake'
require 'erb'
require 'yaml'
require 'html/proofer'

task :default => :test

task :build do
  template = File.read('index.html.erb')
  conferences = YAML.load(File.read('conferences.yml'))
  content = ERB.new(template).result(binding)
  File.write('index.html', content)
end

task :test => :build do
  HTML::Proofer.new('index.html', {
    :typhoeus => {
      :headers => { "User-Agent" => "Mozilla/5.0 (X11; Linux x86_64; rv:10.0) Gecko/20100101 Firefox/10.0" }
  }}).run
end
