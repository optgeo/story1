desc 'host the site'
task :host do
  sh 'budo -d docs'
end

desc 'build config.js from config.conf'
task :config do
  w = File.open('docs/config.js', 'w')
  w.print "var config = #{`parse-hocon config.conf`}"
  w.close
end

