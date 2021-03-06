# IIM
  * Institut de l'internet et du multimédia
  * Spécialité IWM (Ingénérie Web et Mobile)

## dataCollect Project
with python

## cmd important
  * run le notebook : python3 -m jupyter notebook

## Jupyter leçon (quelques tips de base)
  * Executer cellule : shift + enter
  * Markdown : Esc + M
  * Code Python : Esc + Y
  * Supprimer une cellule : ESC => D + D
  * Creer une cellule : Esc => B (en bas) || A (en haut)
  * Code HTML => en mode .md
  * Ecire en mode code : ```language```
  * Id d'un objet : id(var)
  * Type d'un objet : type(var)
  * Montrer les methodes et attributs : dir(var)
  * Premiere lettre en Maj sur str : .capitalize()
  * Faire une fonction : def name ():
  * Class : class Name :
  * Pour ajouter une var à une autre (str, int) : __add__
  * Creer une liste (array) : list() || []
  * Ajouter un elem à une liste : .append()
  * Creer et montrer la docstring : __doc__ && Maj + Tab
  * Longueur d'une liste : len(list var)
  * Afficher une partie de la list : var_list[index1:index2+1]
  * Recuperer l elem index : __getitem__(index)
  * Il est possible de typé les params des function : def name(param: type):
  * Creer un range object dans une list (générer) : list(range(start, stop, step))
  * Dans une class il est possible d avoir le param __self__ à une function pour pointer la class : (ex: def __init__ (self):)
  * Savoir si c'est une instance : (ex: if isinstance(object, int))
  * Str en minuscule : .lower()
  * Str en majuscule : .upper()
  * Remplacer lettres dans str : .replace(old, new)
  * Compter combien de fois une lettre est retourné dans une string : .count(param)
  * Avec Python Str est un itérable
  * Type tuple : (val, val2, val3) => itérable mais pas possible d'assigner un item
  * Pour copier une liste : .copy()
  * Symetrie : tableau 1 ^ tableau 2
  * Appliquer une function à une liste : return ** etc... puis list(map(function, list)) || [function(x) for x in list] | de plus il est possible d utiliser filter()
  * Union : tableau 1 | tableau 2
  * Dans une class il est possible de definir un self pour parler de cette propre instance : exemple (def __init__(self, param))
  * Dans une liste pour prendre les valeurs des items à coté : ex : **dico
  * Intersection : tableau 1 & tableau 2
  * Pour mettre une methode comme instance : @classmethod (peut être appelé directement depuis une instance ou depuis la class) => param = cls
  * Il y a aussi @staticmethod pour englober des functions qui ont la meme finalité (ex: class Max avec des functions calculs mathématiques)
  * Il est possible de hasher : hash(key) || hash(dico[key])
  * Il est possible de creer un dico avec le constructeur dict()
  * Il est possible de selectionner des elems dans un dico dans une loop : .keys() || .values() || .items() => keys + values
  * Pour connaitre la premiere lettre d'une string : str.startwith()
  * Il est également possible de faire heriter les class (class Parent et class Enfant(Parent))
    * avec super().__init__ pour appeler la method parentale (override)
  * Iterable unpacking : var1, var2 = (var1, var2)
    * print("debut {} et fin {}".format(var1, var2))
  * List comprehension et Dict comprehension
    * listB = [elem * 2 for elem in listA] (il est aussi possible de mettre des conditions dedans)
  * Dictionnaire : ensemble (clef:valeur):
    * Acceder à une clef : dico[clef]
    * Supprimer une clef : del avec la valeur pointé
    * Ajouter clef:valeur : Juste rajouter dico[nouvelle_clef] = nouvelle value
  * Pour avoir un nombre random dans un interval :
    * Import random
    * Print(random.randint(number1,number2))
  * Différence entre immutables et mutables :
    * Mutables : Objet que je peux modifier in-situ (ex: list)
    * Immutables : Si je modifie cet objet me retourne un autre object (donc création => ex: valeur d'une var)

  ### Bonus
    * Python Magic Method git : https://rszalski.github.io/magicmethods/
    * Intervenant : https://github.com/Luc-Bertin/IIM_1

  ### Exemple
    * dico : {"cle" : value, "cle2" : value2}
    * decorateurs :
    ```python
    import time

    def deco(func):
      def wrap(x):
        start = time.time()
        result = func(x)
        end = time.time()
        print(end - start)
        return result
      return wrap

    def power(x):
      return x**2

    deco(power)(10)

    ## Ou alors
    @deco
    def power(x):
      return x**2

    print(power(10))
    ```
