== README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:
*CREACION
-Para crear la aplicacion sin los tests que genera por defecto rails :
		rails new sample_app --skip-test-unit

-Ingreso a la carpeta :
		cd sample_app

-Modifico el archivo Gemfile asi :
			source 'https://rubygems.org'
			ruby '2.1.2'
			#ruby-gemset=railstutorial_rails_4_0

			gem 'rails', '4.1.5'

			group :development, :test do
			  gem 'sqlite3', '1.3.8'
			  gem 'rspec-rails', '2.13.1'
			end

			group :test do
			  gem 'selenium-webdriver', '2.35.1'
			  gem 'capybara', '2.1.0'
			end

			gem 'sass-rails', '4.0.3'
			gem 'uglifier', '2.1.1'
			gem 'coffee-rails', '4.0.1'
			gem 'jquery-rails', '3.0.4'
			gem 'turbolinks', '1.1.1'
			gem 'jbuilder', '1.0.2'

			group :doc do
			  gem 'sdoc', '0.3.20', require: false
			end

			group :production do
			  gem 'pg', '0.15.1'
			  gem 'rails_12factor', '0.0.2'
			end

			La salida de la terminal muestra :
				Fetching gem metadata from https://rubygems.org/.........
				Resolving dependencies...
				Using rake 10.3.2
				Using i18n 0.6.11
				Using json 1.8.1
				Using minitest 5.4.1
				Using thread_safe 0.3.4
				Using tzinfo 1.2.2
				Using activesupport 4.1.5
				Using builder 3.2.2
				Using erubis 2.7.0
				Using actionview 4.1.5
				Using rack 1.5.2
				Using rack-test 0.6.2
				Using actionpack 4.1.5
				Using mime-types 1.25.1
				Using polyglot 0.3.5
				Using treetop 1.4.15
				Using mail 2.5.4
				Using actionmailer 4.1.5
				Using activemodel 4.1.5
				Using arel 5.0.1.20140414130214
				Using activerecord 4.1.5
				Using bundler 1.7.2
				Using mini_portile 0.6.0
				Using nokogiri 1.6.3.1
				Using xpath 2.0.0
				Using capybara 2.1.0
				Using ffi 1.9.3
				Using childprocess 0.5.3
				Using coffee-script-source 1.8.0
				Using execjs 2.2.1
				Using coffee-script 2.3.0
				Using thor 0.19.1
				Using railties 4.1.5
				Using coffee-rails 4.0.1
				Using diff-lcs 1.2.5
				Using hike 1.2.3
				Using jbuilder 1.0.2 (was 2.1.3)
				Using jquery-rails 3.0.4 (was 3.1.2)
				Using multi_json 1.10.1
				Using tilt 1.4.1
				Using sprockets 2.11.0
				Using sprockets-rails 2.1.4
				Using rails 4.1.5
				Using rdoc 3.12.2 (was 4.1.1)
				Using rspec-core 2.13.1
				Using rspec-expectations 2.13.0
				Using rspec-mocks 2.13.1
				Using rspec-rails 2.13.1
				Using rubyzip 0.9.9
				Using sass 3.2.19
				Using sass-rails 4.0.3
				Using sdoc 0.3.20 (was 0.4.1)
				Using websocket 1.0.7
				Using selenium-webdriver 2.35.1
				Using sqlite3 1.3.8 (was 1.3.9)
				Using turbolinks 1.1.1 (was 2.3.0)
				Using uglifier 2.1.1 (was 2.5.3)
				Your bundle is complete!
				Gems in the group production were not installed.
				Use `bundle show [gemname]` to see where a bundled gem is installed.

-Modifico el archivo gitignore asi :
			# Ignore bundler config.
			/.bundle

			# Ignore the default SQLite database.
			/db/*.sqlite3
			/db/*.sqlite3-journal

			# Ignore all logfiles and tempfiles.
			/log/*.log
			/tmp

			# Ignore other unneeded files.
			database.yml
			doc/
			*.swp
			*~
			.project
			.DS_Store
			.idea
			.secret
-Verificar que se creo el archivo llamado config/initializer/secret_token.rb (ESTE PASO ME FALLO)


-Ahora ejecuto desde terminal para actualizar las gemas instaladas :
			bundle update

			Esta es la salida de la terminal :

			Fetching gem metadata from https://rubygems.org/.........
			Resolving dependencies...
			Using rake 10.3.2
			Using i18n 0.6.11
			Using json 1.8.1
			Using minitest 5.4.1
			Using thread_safe 0.3.4
			Using tzinfo 1.2.2
			Using activesupport 4.1.5
			Using builder 3.2.2
			Using erubis 2.7.0
			Using actionview 4.1.5
			Using rack 1.5.2
			Using rack-test 0.6.2
			Using actionpack 4.1.5
			Using mime-types 1.25.1
			Using polyglot 0.3.5
			Using treetop 1.4.15
			Using mail 2.5.4
			Using actionmailer 4.1.5
			Using activemodel 4.1.5
			Using arel 5.0.1.20140414130214
			Using activerecord 4.1.5
			Using bundler 1.7.2
			Using mini_portile 0.6.0
			Using nokogiri 1.6.3.1
			Using xpath 2.0.0
			Using capybara 2.1.0
			Using ffi 1.9.3
			Using childprocess 0.5.3
			Using coffee-script-source 1.8.0
			Using execjs 2.2.1
			Using coffee-script 2.3.0
			Using thor 0.19.1
			Using railties 4.1.5
			Using coffee-rails 4.0.1
			Using diff-lcs 1.2.5
			Using hike 1.2.3
			Using jbuilder 1.0.2
			Using jquery-rails 3.0.4
			Using multi_json 1.10.1
			Using tilt 1.4.1
			Using sprockets 2.11.0
			Using sprockets-rails 2.1.4
			Using rails 4.1.5
			Using rdoc 3.12.2
			Using rspec-core 2.13.1
			Using rspec-expectations 2.13.0
			Using rspec-mocks 2.13.1
			Using rspec-rails 2.13.1
			Using rubyzip 0.9.9
			Using sass 3.2.19
			Using sass-rails 4.0.3
			Using sdoc 0.3.20
			Using websocket 1.0.7
			Using selenium-webdriver 2.35.1
			Using sqlite3 1.3.8
			Using turbolinks 1.1.1
			Using uglifier 2.1.1
			Your bundle is updated!
			Gems in the group production were not installed.

-A continuación, tenemos que configurar Rails utilizar RSpec en lugar de Test::Unit
			rails generate rspec:install

			La salida del terminal es :
				create  .rspec
			      create  spec
			      create  spec/spec_helper.rb
 
 -Ahora inicializo un repositorio git :
 			git init
 			git add .
 			git commit -m "Commit Inicial"

 -

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions






== README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:
*CREACION Y PASOS



-Modifico el archivo .gitignore asi :
		# Ignore bundler config.
		/.bundle

		# Ignore the default SQLite database.
		/db/*.sqlite3
		/db/*.sqlite3-journal

		# Ignore all logfiles and tempfiles.
		/log/*.log
		/tmp

		# Ignore other unneeded files.
		database.yml
		doc/
		*.swp
		*~
		.project
		.DS_Store
		.idea
		.secret

-










Please feel free to use a different markup language if you do not plan to run
<tt>rake doc:app</tt>.
