# Projet final



I - Contexte du projet
----------------------
La crise du covid a durement éprouvé le monde et les entreprise n'en sont pas restées en marge.Nombreuses d'entre elles ont décidé de se réinventées en s'appuyant sur l'outil informatique pour étendre leurs activités.C'est le cas de la société JEVENEDSENLIGNE.

La société JEVENEDSENLIGNE était une entreprise spécialisée dans la distribution d'articles mais cela de manière physique.Avec la crise du covid, elle a décidé de se créer un espace sur la toile afin de faciliter ses ventes.Pour se faire,elle vous a fait appelle en tant que développeur web java afin que vous l'accompagner dans ce projet.



II - Fonctionnalités du projet
-----------------------------
ILs existent trois grands acteurs dans ce projet qui sont :
- l'internaute (personne ne possédant pas encore de compte sur la plateforme ou qui n'est peut être connecté au moment de la visite du site)
- Le client (personne possédant un compte et qui est connecté au moment de la visite de la plateforme)
- L'agent backoffice (Employé de la société qui est chargé de l'animation de la plateforme)

Les fonctionnalités de la dite plateforme sont les suivantes:

   1 - En tant qu'agent backoffice

      - Je peux créer,modifier,voir le détail et supprimer un catalogue de produit ou catégorie de produit.

     - Je peux créer,modifier,voir le détail et supprimer un produit.

     - Je peux voir la liste des clients inscrits sur la plateforme
     - Je peux créer, modifier, voir le détail et supprimer les commandes (si elle a un état annulé) des clients
  2 - En tant que Client
    
    - Je peux me connecter à la plateforme
    - Je peux rechercher un produit à partir de son libellé
    - Je peux créer une commande et la valider (pour le paiement de la commande une simulation sera effectuée)
    - Je peux voir la liste de mes commandes et annuler mes commandes (seulement si cette dernière à un état encours de livraison)

  3 - En tant qu'internaute
  - Je peux voir le catalogue de produit
  - Rechercher un produit à partir de son nom
 


II - Conseils de dévéloppement
------------------------------

- Les commandes doivent avoir les états suivants : ENCOURS, ANNULE, SUPPRIMEE (Vous pouvez utilisez les enumerations en Java)
- IL faudrait utiliser le templating pour la mise en place du site web
- Pour l'affichage des données dans la liste vous pouvez utilisez les datables de Jquery avec pagination (client/serveur)

III - Exigences

- Les technologies à utiliser sont les suivantes : 
    - Frontend : JSP,JSLT, Javascript
    - Backend : Postgresql 12(Base de données), Jakarta EE 10 (Servlets,JPA,Widfly 27)
    - Git et Github
    - La solution deployé doit être un war

