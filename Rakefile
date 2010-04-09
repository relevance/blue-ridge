require "rubygems"
require "micronaut"
require "micronaut/rake_task"

ENV["BLUE_RIDGE_PREFIX"] = File.dirname(__FILE__)
import File.dirname(__FILE__) + '/lib/tasks/javascript_testing_tasks.rake'

namespace :test do
  desc "Run all micronaut examples using rcov"
  Micronaut::RakeTask.new :rubies do |t|
    t.pattern = "spec/rubies/**/*_spec.rb"
  end
end

task :default => ["test:rubies", "test:javascripts"]