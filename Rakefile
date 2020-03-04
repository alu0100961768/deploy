require 'html-proofer'

task :test do
  sh "bundle exec jekyll build"
  options = { :assume_extension => true,
              :allow_missing_href => true,
              :allow_hash_href => true,
              :disable_external => true,
            }
  HTMLProofer.check_directory("./_site", options).run
end

desc "Test the website"
task :test2 do
  options = {
    :check_sri => true,
    :check_external_hash => true,
    :check_html => true,
    :check_img_http => true,
    :check_opengraph => true,
    :enforce_https => true,
    :cache => {
      :timeframe => '6w'
    }
  }
  begin
    HTMLProofer.check_directory(".", options).run
  rescue => msg
    puts "#{msg}"
  end
end

task :myraketask do

  begin
      1/1
  rescue
      puts "not failing :)"
  end
  
end