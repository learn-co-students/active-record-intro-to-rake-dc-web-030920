
namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  task :hola do
    puts 'hola de Rake!'
  end
end

  desc 'drop into the Pry console'
  task :console => :environment do
    Pry.start
  end

  namespace :db do

    desc 'Creates the Student table'
    task :migrate => :environment do
      Student.create_table
    end

    desc 'Invokes the environment task as dependency'
    task :environment do
      require_relative './config/environment'
    end

    desc 'Seeds the database with dummy data from seed file'
    task :seed do
      require_relative './db/seeds.rb'
    end

  end