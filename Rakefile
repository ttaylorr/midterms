task :default => [:compile]

desc "Compile all *.tex files into pretty PDFs"
task :compile do
  sh 'rubber --force --inplace --pdf ./**/*.tex'
  Rake::Task["clean"].invoke
end

desc "Cleanup all the cruft that was generated by rubber"
task :clean do
  ["aux", "log", "dvi", "toc"].each do |ext|
    # Delete all the garbage files, supress output of stdout and stderr to
    # /dev/null
    `rm ./**/*.#{ext} 2&>1 > /dev/null`
  end
end
