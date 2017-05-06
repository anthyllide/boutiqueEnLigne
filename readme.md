Mini site de vente en ligne d�vellop� avec le framework Symfony 2.8
===================================================================

Fichiers
--------

Le fichier sil11.sql contient la BDD.

Page d'accueil
--------------

"Le top 3 des articles les plus vendus" s'affiche par un contr�leur imbriqu�.
Un r�pository personnalis�, Order_lineRepository g�re une requ�te sql pour s�lectionner les articles en plus vendus 
en fonction des quantit�s qui ont �t� vendus.

Page catalogue
--------------

Affiche les cat�gories disponibles.

Page articlesparCategorie
-------------------------

Affiche les articles par cat�gorie

* De l� l'utilisateur peut soit directement ajouter un article au panier ou acc�der � la fiche produit de l'article
* Si le produit n'a pas de stock, le bouton "ajouter au panier" est remplac� par "en cours de r�approvisionnement"

Page article (fiche produit)
----------------------------

Affiche toutes les informations d'un produit avec sa photo

L'utilisateur peut ajouter au panier le produit

Page contenuPanier
------------------

Affiche le panier et calcule le total TTC, dont la TVA.

L'utilisateur peut ajouter ou diminuer la quantit�, supprimer un article ou vider tout le panier.

* Si l'utilisateur diminue la quantit� en-dessous de 1, l'article est supprim� du panier.

* Si l'utilisateur augmente la quantit� au-dessus du stock disponible, un message informe l'utilisateur et le quantit� n'augmente plus.

* Le nombre d'articles diff�rents s'affiche en haut � droite du menu haut.

Page Valider panier
-------------------

Quand l'utilisateur valide son panier, s'il n'est pas authentifi�, le formulaire de connexion s'affiche, sinon un message informe le client 
du num�ro de sa commande.

* Le stock des articles command�s est d�compt�.

Utilisateurs
------------

Le site compte 3 utilisateurs.

* Anonyme
* USER = les clients authentifi�s
* ADMIN = Administrateurs

* Un compte administrateur : 
** email : choucaxa@hotmail.fr
** mdp : alex

* Un compte client :
** email : e.bel@orange.fr
** mdp : bel

Quand un client se connecte, le menu haut �volue :
* A la place de "votre compte", un "bonjour pr�nom du client" apparait, et il a acc�s � partir de ce menu � :
** votre compte : ses informations (nom, pr�nom, email) s'affichent et le client peut les modifier, y compris son mot de passe.
** vos commandes : les commandes du client s'affiche

Quand un administrateur se connecte, le menu haut �volue comme les clients, mais l'onglet "Admin" apparait en plus.

Espace Admin
------------

##Page Admin

La page admin n'est accessible que par les administrateurs. Elle donne acc�s au back-office du site.

##Menu Cat�gorie

Permet d'afficher les cat�gories du site, de les modifier, de les supprimer et d'en cr�er une nouvelle.

##Menu Article

Permet d'afficher les articles du site, de les modifier, de les supprimer et d'en cr�er un nouveau.

##Menu Commande

Permet d'afficher les commandes et de les valider ou non.

