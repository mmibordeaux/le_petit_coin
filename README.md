# README

## App en local 

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