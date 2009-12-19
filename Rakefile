task :default => "doc:gen"

namespace :doc do
  desc "Generates documentation"
  task :gen do
    sh "asciidoc -a max-width=55em -a toc *.adoc"
  end
end
