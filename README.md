# Projet de Python pour la data science (ENSAE 2A)
Auteurs : Philippe de Tinguy, Marine Huchet et Nicolas Nogueira

Ce projet a pout but d'explorer les liens entre la croissance économique et la déforestation des pays depuis 2001. Plus précisément, après avoir étudié les données de façon descriptives grace à des graphiques et des cartes, nous allons essayer de modéliser la relation entre le PIB, sa croissance et la déforestation/production de bois avec des modèles économétriques.

Pour explorer le projet, il suffit d'utiliser le notebook Main.ipynb qui contient tout le code et les résultats commentés. 

Le code pour récupérer nos données est tout de même dans d'autres notebooks pour ne pas surcharger le principal. Il n'est pas nécessaire de les ouvrir et de les faire tourner séparément pour accéder aux données puisque celles si sont soit disponibles en csv soit le code permettant de les générer est appelé dans le notebook principal.

Les données proviennent de trois sources différentes : 
- la Food and Agriculture Organization (FAO) : le fichier csv brut est récupéré directement sur le site de la FAO et est nommé Données_FAO.csv - le notebook API FAO et FAOSTAT.ipynb  explique pourquoi cela a été nécessaire. Le CSV est ensuite modifié et mis en forme dans le notebook Traitement_FAO.ipynb puis enregistré sous le nom data_FAO_final.csv
- Global Forest Watch : les données sont récupérées grâce à un package sur python dans le notebook API_OWID.ipynb, puis enregistrées en csv sous le nom df_owid.csv
- la Banque Mondiale : les données sont récupérées par API dans le notebook API_banque_mondiale.ipynb, et enregistrées sous le nom data_BM.csv

Le document requirements.txt contient tous les modules que nous devons installer pour faire fonctionner notre code (l'installation se lance automatiquement dans Main). 

Finalement, nous avons réussi à créer un modèle économétrique qui relie données de la déforestation et de la production de bois au PIB, permettant de l'estimer avec une certaine précision. Cependant, aucun lien n'a pu être fait entre croissance économique et déforestation ou production de bois. Si cela ne signifie pas que celles-ci sont indépendantes, cela vient corroborer l'idée que la déforestation n'a pas de gains économiques réels - et donc qu'il vaudra mieux protéger ses espaces naturels. 

