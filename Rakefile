require "rubygems"

port = 8000 + Random.rand(1000)

task :launch do
  %x{sleep 1}
  %x{open http://localhost:#{port}}
end

task :server do
  puts "starting presentation..."
  %x{python -m SimpleHTTPServer #{port}}
end

multitask :start => [:server, :launch]

task :default => :start
