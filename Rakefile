require "rubygems"

task :launch do
  %x{sleep 1}
  %x{open http://localhost:8000}
end

task :server do
  puts "starting presentation..."
  %x{python -m SimpleHTTPServer 8000}
end

multitask :start => [:server, :launch]

task :default => :start
