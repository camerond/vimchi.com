require 'dotenv'
Dotenv.load

desc "Deploy site"
task :deploy do
  system "middleman build --clean"
  system "rsync -av --no-p --chmod=+r -e ssh --delete build/ #{ENV['DEPLOY_TARGET']}"
end
