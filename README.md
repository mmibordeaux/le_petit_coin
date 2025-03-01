# README

## App en local 

```bash
rails new le_petit_coin --skip-solid --database=postgresql 
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

## Github

Puis on envoie sur Github
```bash
git add .
git commit -m "init"
```

Sur votre Github, créer un repo (ici, mmibordeaux/le_petit_coin)
```bash
git remote add origin git@github.com:mmibordeaux/le_petit_coin.git
git push --set-upstream origin main
```

## Scalingo

Créer l'app (la nommer)

Choisir de la lier à Github


Ajouter ça au Gemfile 

```rb
ruby "3.4.1"
```

Mettre à jour le bundle 
```bash
bundle update --ruby
```

Supprimer le dossier `.github`

Sur Scalingo, provisionner une base PostgreSQL (dans les ressources, addon)

Créer un fichier `Procfile`

Mettre ça dedans 
```
web: bundle exec puma -C config/puma.rb
postdeploy: rails db:migrate
```

Envoyer sur Github

## Bootstrap


Suivre cette doc :

https://medium.com/@xnjiang/how-to-use-bootstrap-in-rails8-cd0d53f1c3bc


Ajouter la config Simple Form pour Boostrap :
```bash
rails generate simple_form:install --bootstrap
```

Démarrer le serveur avec cette commande (et pas rails server) 
```bash
bin/dev
```

## Devise

On suit l'install de devise
https://github.com/heartcombo/devise?tab=readme-ov-file#getting-started

```bash
bundle add devise
rails generate devise:install
rails generate devise User
rails db:migrate
````

