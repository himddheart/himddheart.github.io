# coding: utf-8
task default: %w[serve]

task :init do
	sh "bundle install"
end

task :serve do
	sh "bundle exec jekyll serve"
end
task :build do
	sh "rm -rf ./_site"
	sh "bundle exec jekyll build --destination=../site"
	sh "rm -rf ./_site"
end

task :deploy do
	sh "git add ../site"
	sh "git commit -m \"Deployed at #{Time.now}\""
	sh "git push"
end

