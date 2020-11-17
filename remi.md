# MARHCHE A SUIVRE A CHAQUE NOUVEAU PROJET


## A CHAQUE NOUVELLE APPLICATION
* rails new -d postgresql nomdetasuperappli --skip-turbolinks
* cd nomdetasuperappli/
* open nomdetasuperappli/Gemfile
    replace gem 'tzinfo-data', platforms: [:mingw, :mswin, :x64_mingw, :jruby]
      par 
            # gem 'tzinfo-data', platforms: [:mingw, :mswin, :x64_mingw, :jruby]
            group :development do
              gem 'better_errors'
              gem 'binding_of_caller'
              gem 'letter_opener'
            end
            # gem 'execjs'
            # gem 'therubyracer'
            gem 'table_print'
            gem 'faker'
            gem 'dotenv-rails'
            gem 'bcrypt'
            # gem 'jquery-rails'
            # gem 'bootstrap'
            gem 'devise'
            group :production do
              gem "aws-sdk-s3", require: false
            end
            gem 'mini_magick'
            gem 'image_processing'
* dans le fichier app/views/layouts/application.html.erb, ajoute Bosstrap :
  * Ajouter au début:
        <!-- Bootstrap CSS -->
        <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.2.1/css/bootstrap.min.css" integrity="sha384-GJzZqFGwb1QTTN6wy59ffF1BuGJpLSa9DkKMp0DgiMDm4iYMj70gZWKYbI706tWS" crossorigin="anonymous">
        <!-- Biblio d'Icones -->
        <script src="https://kit.fontawesome.com/dc9a3c0907.js" crossorigin="anonymous"></script>
  * Ajouter a la fin:
      </body>
      <!-- Optional JavaScript -->
      <!-- jQuery first, then Popper.js, then Bootstrap JS -->
      <script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
      <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js" integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1" crossorigin="anonymous"></script>
      <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js" integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM" crossorigin="anonymous"></script>
    </html>
* bundle install


## BASE DE DONNEES POSTGRESQL
* rails db:create
* rails db:migrate
* rails db:seed
* rails generate devise:install


## CONFIG MAILER
* dans le fichier config/environments/development.rb
  * ajouter config.action_mailer.default_url_options = { host: 'localhost', port: 3000 }
* in config/environments/production.rb
  * ajouter config.action_mailer.default_url_options = { :host => 'YOURAPPNAME.herokuapp.com' }


## CONFIG AUTHENTIFICATION ET GESTION USER
* rails g devise User
* rails g devise:views


## CONFIG GRAPHIQUES
* créer les sous-dossiers suivants :
  * lib/assets/
  * lib/assets/stylesheets/
  * lib/assets/javascripts/
  * vendor/assets/
  * vendor/assets/stylesheets/
  * vendor/assets/javascripts/
* ajouter les chemins créés dans : config/initializers/assets.rb
  * Rails.application.config.assets.paths << Rails.root.join("lib", "assets", "stylesheets")
  * Rails.application.config.assets.paths << Rails.root.join("lib", "assets", "javascripts")
  * Rails.application.config.assets.paths << Rails.root.join("vendor", "assets", "stylesheets")
  * Rails.application.config.assets.paths << Rails.root.join("vendor", "assets", "javascripts")
* ce qui donne par exemple
  * ├── app/assets/stylesheets/
  * │   ├── application.css
  * │   ├── main.css
  * │   └── day.css
  * ├── lib/assets/stylesheets/
  * │   └── acme_ui_kit.css
  * ├── vendor/assets/stylesheets
  * └── bootstrap.css
* dans le fichier :app\assets\stylesheets\application.css
  * retirer:
  * *= require_tree .
  * *= require_self
* ajouter pour correspondre a l'exemple:
  * /* ...
  * *= require bootstrap
  * *= require acme_ui_kit
  * *= require main
  * *= require day
  * */
* créé le dossier app/assets/fonts/


## Stockage d'image
* rails active_storage:install
* gem 'mini_magick'
* gem 'image_processing'
* sudo apt-get install imagemagick 


## PARAMS CLEES D'API
* Crée un fichier .env à la racine de ton application.
* Ouvre-le et écris dedans les clés (ex: SENDGRID_LOGIN='apikey' et SENDGRID_PWD='ta_clef_API')
* Ouvre le fichier .gitignore à la racine de ton app Rails et écris .env dedans


## MEP
* rails assets:precompile
* rails assets:clean
* RAILS_ENV=production RAILS_SERVE_STATIC_FILES=true rails server
* Tester l'appli en mode production
* heroku create nom-de-ton-app
* git push heroku master
* heroku run rails db:migrate (si tu as une migration à migrer)
* heroku run rails db:seed
* Créé tes clés d'API en prod : heroku config:set SENDGRID_LOGIN='apikey' SENDGRID_PWD='ta_clef_API'


## PB de Yarn:
* yarn add bootstrap
* yarn add jquery popper.js 