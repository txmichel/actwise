require 'html/proofer'

desc 'Build for deployment (but do not deploy)'
task :build do
  jekyll("build --config _config.yml")
end

task :test do
HTML::Proofer.new(
  "./_site",
  # hacks to get html proof to pass links we wanted ignored
  href_swap: {
    'http://blog.actwise.de' => '', # canonical link in head
  }
).run
end

# launch jekyll
def jekyll(directives = '')
  sh 'bundle exec jekyll ' + directives
end
