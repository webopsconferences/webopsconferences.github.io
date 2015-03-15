require 'rake'
require 'erb'
require 'yaml'

task :default => :test

task :build do
  template = File.read('index.html.erb')
  conferences = YAML.load(File.read('conferences.yml'))
  content = ERB.new(template).result(binding)
  File.write('index.html', content)
end

task :test => :build do
  status = system('htmlproof index.html')
  exit status
end
