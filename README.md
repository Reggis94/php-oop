L'injection de dependance est un moyen qui permet d'éviter que plusieurs objets soit interdependant en séparant bien les taches de chaque objet.
Par exemple si une personne possède une adresse alors, le constructeur de Person ne sera pas:

construct(street, city, region){}

Mais plutôt

construct(Address address)

Comme ça, si nous devons modifier les formats d'uhe adresse alors on modifiera seulement la classe adresse.

Le patern Observer est utilisé lorsqu'il y a une relation de type One To Many entre des objets.
Le but de ce pattern est de faire en sorte que si un objet est modifié alors les autres objets doivent être notifié du changement.

Par exemple, nous pouvons avoir une classe Person qui a un age comme propriété.
En liant la classe Person à un Observer par exemple un ObserverBinary, dès l'année n+1,
ObserverBinary sera en mesure de constater le changement dans sa proporiété personne de la classe Person grâce à une méthode que 
nous pouvons appeler notifyObserver qui se chargera d'utiliser une fonction update dans l'Observer.


Le temporal coupling est le fait de devoir executer des méthodes dans un ordre précis à chaque fois.
Le problème du temporal coupling est que des erreurs peuvent être générer si on oublie l'ordre spécifique des instructions à réaliser.
Par exemple si on doit systématiquement convertir des sommes d'argent, des erreurs sur le prix final peuvent avoir lieu à cause du temporal coupling.
La solution serai d'avoir par exemple pour un article un constructeur de ce style:

Article(price, conversionRate);

Le développeur ne pourra pas se tromper puisqu'il sera obliger d'insérer la conversion nécessaire.
