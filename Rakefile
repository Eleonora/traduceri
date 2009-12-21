task :default => :docs

FILES = Dir["*.adoc"]
PAGES = FILES.map {|f| "#{f.gsub(/adoc$/, '')}html"}

PAGES.each do |html|
  txt = File.basename(html).gsub(/html$/, 'adoc')

  file html => [txt] do |t|
    sh "asciidoc -a max-width=55em -a toc -a toc-title=Cuprins -o #{t.name} #{txt}"
  end
end

task :docs => [:init, :compile]
task :compile => PAGES

task :init do
  # mkdir_p "out"
end
