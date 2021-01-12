---
layout: default
title: Renault ZE
description: Plugin d'interfaçage avec les Véhicules Renault ZE
---

# Présentation

Ce plugin permet la communication entre votre véhicule Renault ZE et Jeedom.

Il permet de :

- connaître l'état courant de votre voiture (charge de la batterie, autonomie, kilométrage...),
- lancer des actions sur votre véhicule depuis Jeedom (démarrage du préconditionnement, activation du planning de charge...).

# Configuration

Dans la configuration générale du plugin, vous devez reneigner vos identifiants sur le portail Renault ou l'application Android ou iOS.

À chaque validation de cette configuration, le plugin récupère la liste des véhicules enregistrés. (Dans les versions récentes de Jeedom, il faut souvent rafraîchir la page du navigateur pour voir les nouveaux objets).

Les véhicules sont identifiés par leur immatriculation. Il faut ensuite activer et désactiver les commandes directement dans l'objet.

## Configuration de l'équipement

Dans la page de configuration de l'équipement, vous pouvez configurer :

- la température de préconditionnement (Pour l'instant, Renault ne semble accepter que 21 comme valeur, mais il est prévu dans l'API de pouvoir passer une autre valeur)
- le lien vers un objet Geoloc. Ce paramètre est utile uniquement pour les Zoé2. Cela vous permet de remonter dans Jeedom la position de votre Zoé quand celle ci est mise à jour sur les serveurs. Cette position peut ensuite être utilisée dasn des scénarios Jeedom par exemple.

# FAQ

Les commandes sont disponibles ou non selon le type de véhicule. La localisation n'est disponible que sur les Zoé2. Selon les modèles de véhicules, il est également possible que les services renvoient des valeurs avec des unités différentes (sur le courant de charge par exemple, les Zoé 1 renvoient une valeur en W, les Zoé 2 en kW).

# Troubleshooting

Si certaines commandes principales du plugin (hVac, schedule notamment) ne fonctionnent plus du jour au lendemain, il est fortement probable qu'un de vos abonnements Renault est arrivé à échéance. Le plugin teste la validité des abonnements tous les jours et écrit une trace en debug si un abonnement nécessaire n'est pas dispo. Il vous suffit donc de passer les traces du plugin en debug pour controler l'etat de vos abonnements.
