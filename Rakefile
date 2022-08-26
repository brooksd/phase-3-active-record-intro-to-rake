namespace :greeting do
  desc "outputs hello to the terminal"
  task :hello do
    puts "hello from Rake!"
  end

  desc "First Rake task"
  task :maker do
    puts "Brooks is Here!"
  end
end

task :environment do 
  require_relative './config/environment'
end

namespace :db do
  desc 'migrate changes to your database'
  task migrate: :environment do
    Student.create_table
  end

  desc 'seed the database with some dummy data'
  task seed: :environment do 
    require_relative './db/seeds.rb'
  end
end

desc 'drop into the pry console'
task console: :environment do
  Pry.start
end