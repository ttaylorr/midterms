task :default => [:compile]

desc "Compile all *.tex files into pretty PDFs"
task :compile do
  sh 'rubber --force --inplace --pdf ./**/*.tex'
end
