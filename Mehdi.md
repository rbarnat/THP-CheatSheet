## Les Tests
Pour pouvoir tester tes projets ruby voila la procèdure à suivre :

* commence par installer la gem `rspec` avec la commande :
```language-shell
$ gem install rspec
```

* Si ton programme se nomme `hello_world.rb` alors tu devras nommer ton programme de test `hello_world_spec.rb`

* Ton dossier doit avoir cette structure : 

``` language-shell
my_super_test_project
├── lib
│   ├── hello_world.rb
│   └── ton_deuxième_programme.rb
├── spec
│   ├── spec_helper.rb (un fichier de configuration de rspec)
│   └── hello_world_spec.rb
└── .rspec</code>
```

* Installe `rspec` dans ton dossier de travail maintenant :
```language-shell
$ rspec --init
```

* Un fichier de test aura cette allure-là :
```ruby
require_relative '../lib/hello' //fait appel au programme testé

describe "the hello function" do //décrit un groupe de test
  it "says hello" do //décrit un test plus précis au sein du groupe qui se focalise sur une fonction
    expect(hello).to eq("Hello world!") //test si ta méthode ou variable renvoie le bon résultat
  end
end
```

•	Lance ton test en te mettant à la racine de ton dossier projet avec la commande :

```language-shell
$ rspec
```

N’oublie pas qu’il ne faut pas avoir d’espace dans le chemin d’accès aux fichiers 😉

## Bien écrire son code en Ruby

* Les indentations de Ruby sont de 2 espaces
* Les noms de variables, fichiers et méthodes doivent être en anglais, bien explicites et en snake_case, examples : `appartment_price` pour une variable, `appartment_price_array` pour un array
* Les noms de classes ou modules doivent être en CamelCase 
* La gem `Rubocop` peut t'aider à suivre les bonnes conventions

## Gérer ses gems

* pour installer une gem : 

```language-shell
$ gem install nom-de-ta-gem
```

* pour voir la liste des gems installées : 

```language-shell
$ gem list
```

* pour installer à partir d'un Gemfile : 

```language-shell
$ bundle install
```

## ASCII Ruby

* Pour passer d'un caractère au nombre ASCII correspondant utilise `.ord`, example pour la lettre "A" : `"A".ord` (si tu oublie les guillemets autour de "A" il ira chercher une variable A)
* Pour passer du nombre ASCII au caractère utilise `.chr`, example : `65.chr` te renvoie "A"
