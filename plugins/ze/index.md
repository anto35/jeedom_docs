# Renault ZE

## Présentation

Ce plugin permet la communication entre votre véhicule Renault ZE et Jeedom.

Il permet :

- De connaître le statut courant de votre voiture ( Charge de la batterie, autonomie, kilométrage, ... ) 

- Permettre de lancer des actions sur votre véhicule depuis Jeedom (Démarrage du préconditionnement, activation du planning de charge, ...)

## Configuration

Dans la configuration générale du plugin, vous devez reneigner vos identifiants sur le portail Renault ou l'application Android ou iOS.

A chaque validation de cette configuration, le plugin récupère la liste des véhicules enregistrés. (Dans les versions récentes de Jeedom, il faut suvent rafraîchir la page du navigateur pour voir les nouveaux objets).

Les véhicules sont identifiés par leur immatriculation. Il faut ensuite activer et désactiver les commandes directement dans l'objet.

## FAQ

Si votre Zoé ne remonte plus d'infos ni dans l'appli Renault ni dans le plugin Jeedom, il se peut que votre abonnement soit échu. Pour renouveler, il faut vous rendre sur le portail MyRenault, vous connecter avec vos identifiants, dans le meu RLinkStore sélectionner l'item ZE Connect, et suivre la procédure d'installation dans la voiture.
