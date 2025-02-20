# README

```bash
rails new --skip-solid --database=postgresql le_petit_coin
cd le_petit_coin
bundle add simple_form
rails generate simple_form:install
rails generate scaffold user pseudonym:string photo:string
rails db:migrate
rails s
```

Dans le fichier `config/routes.rb`, ajouter une route racine : 

```ruby
  root "users#index"
```