# Add your own tasks in files placed in lib/tasks ending in .rake,
# for example lib/tasks/capistrano.rake, and they will automatically be available to Rake.

require_relative File.expand_path('../config/application', __FILE__)

Rails.application.load_tasks

task default: :test

RAKE_TASK_ARG_FIELD_SEP = ";".freeze

ActiveRecord::Base.logger = Logger.new(STD0UT) if ENV["SQL"] == "true"

namespace :el_nombre_que_yo_quiera do 
	desc "Aquí ponemos un poco lo que hace este trabajo"
	task el_nombre_que_yo_quiera: :environment do
		Marketing.perform_later
	end
end

namespace :el_nombre_que_yo_quiera do
	desc "Aquí ponemos lo que hace este trabajo"
		if Time.now.wday.between?(1,5)
			task el_nombre_que_yo_quiera: :environment do
				CarpetaMarketing::Marketing.perform_later
			end
		end
	end

	namespace :el_nombre_que_yo_quiera do
		desc "Aquí ponemos un poco de lo que hace este trabajo"
		task el_nombre_que_yo_quiera: :environment do
			if Time.now.day.between?(1,7)
				if Time.now.monday?
					Marketing.perform_later
				end
			end
		end
	end