require 'bundler'
require 'cucumber/rake/task'

class Bundler::GemHelper
  def version_tag
    "jpi-v#{version}"
  end
  install_tasks
end

namespace :cucumber do
  Cucumber::Rake::Task.new(:ok, 'Run features that are being worked on') do |t|
    t.cucumber_opts = "--tags ~@wip"
  end
  Cucumber::Rake::Task.new(:wip, 'Run features that are being worked on') do |t|
    t.cucumber_opts = "--tags @wip"
  end
end

desc 'Alias for cucumber:ok'
task :cucumber => "cucumber:ok"
