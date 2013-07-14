require 'stringex'

def post_title? message
  print message
  STDIN.gets.chomp
end

desc "Create a new post"
task :new do
  title = post_title?('Title: ')
  filename = "content/posts/#{Time.now.strftime('%Y-%m-%d')}-#{title.to_url}.md"

  if File.exist? filename
    puts "Can't create new post: \e[33m#{filename}\e[0m"
    puts " \e[31m- Path already exists.\e[0m"
    exit 1
  end

  File.open(filename, "w") do |post|
    post.puts '---'
    post.puts "title: \"#{title}\""
    post.puts "created_at: #{Time.now}"
    post.puts 'kind: article'
    post.puts 'published: false'
    post.puts "---\n\n"
    post.puts "Once upon a time..."
  end

  puts "A new post was created at:"
  puts " \e[32m#{filename}\e[0m"
end

task :generate do
  system 'nanoc compile'
end

desc 'Generate and deploy'
task :deploy => :generate do
  sh 'rsync -rtzhv --progress --delete-after output/ deploy@193.183.99.122:/srv/rubyjams.org/production/'
end

