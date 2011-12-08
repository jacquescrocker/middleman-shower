namespace :github do
  desc "Build and deploy to github"
  task :deploy do
    # set up repo
    repo = ENV["REPO"]
    repo ||= begin
      origin_remote = `git remote show origin`
      origin_remote.match(/(\w)*URL:(.)*\n*/).to_s.split(":")[1..-1].join(":").strip
    end

    if repo == nil or repo == ""
      puts "ERROR: can't find a valid repo. Use rake REPO=git@github.com:username/repo.git deploy:github to override"
      return
    end

    puts "Building middleman..."
    puts `rm -Rf ./build`
    puts `middleman build`

    puts "Deploying to github (#{repo})..."
    puts `cd ./build && git init`
    puts `cd ./build && git add .`
    puts `cd ./build && git commit -m 'regenerating'`
    puts `cd ./build && git checkout -b gh-pages`
    puts `cd ./build && git remote add github #{repo}`
    puts `cd ./build && git push github gh-pages --force`
  end
end