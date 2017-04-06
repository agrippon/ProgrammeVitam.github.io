---
layout: page
title: Ressources
fatherref: ressources
level: page
---

> Est ici présenté l'ensemble des ressources mises à disposition concernant les versions actuelle et passées de la solution logicielle Vitam. 

## Solution logicielle Vitam - dernière version publiée ({{ site.version }})

Il s'agit du logiciel Vitam proprement dit, réunissant le back-office et les différentes IHM. Sont mis à dispostion:

* **le code développé**

Il est accessible sur GitHub dans le dépot GitHub [{{ site.github.repo }}]({{ site.github.repo }}).

* **les packages java (.jar) associés, diffusés pour Maven**

Ils sont accessibles sur BinTray [{{ site.bintray.repomaven }}]({{ site.bintray.repomaven }}).

* **les paquets de déploiement** 

Ils permettent d'installer de manière outillée la solution, sous forme RPM 
CentOS 7. Ils contiennent aussi des conteneurs de documentation et de jeux de 
tests. Ils sont accessibles sur BinTray [{{ site.bintray.repo }}]({{ site.bintray.repo }}).

* **la documentation fonctionnelle et technique**

Elle est accessible, en partie  sur GitHub pour les documents en forme brute RST, intégralement dans les packages sur Bintray, mais aussi directement sous forme PDF et/ou HTML sur la page [Documentation](/pages/documentation)

* **les jeux de tests**

Ils contiennent les référentiels de test, et les fichiers SIP utiles pour les 
tests automatiques. *A noter qu'il faut injecter les référentiels avant de lancer les tests.*
Ils sont accessibles sur BinTray [{{ site.bintray.repodataset }}]({{ site.bintray.repodataset }}).

## Outils complémentaires Vitam - dernière version publiée ({{ site.version }})

Il s'agit des outils utilisés pour faciliter le test ou le développement. 

Pour 
le moment, il s'agit du **Générateur Seda**, un outil de développement permettant
de générer automatiquement à partir d’une simple arborescence de fichiers un SIP
(paquet d’information à archiver) conforme aux [recommandations Vitam](/ressources/Doc0.11.1/20170116_Design_SIP_beta_V1.4.pdf).
 Sont mis à dispostion:

* **le paquet d'installation sous Linux et Windows**

Il s'agit d'un conteneur zip à décompresser en local et dont l'exécution 
nécessite seulement la présence de java 8 sur le poste 
([zip](/ressources/Res0.11.1/generateur-seda_0.11.1.zip)).

* **une présentation du Générateur Seda**

Elle décrit les fonctions du Générateur ainsi que son utilisation simple et avancée
([pdf](/ressources/Res0.11.1/20170116_presentation_generateur_V1.0.pdf)).

* **le code développé**

Il est accessible dans le dépot GitHub [{{ site.github.repoext }}]({{ site.github.repoext }}). A noter que les packages java (.jar) sont sur le même point Maven que la solution logicielle.


<br>
<hr/>

## Anciennes ressources

### API alpha

* Package de présentation ([zip](/ressources/API-Alpha/Vitam-API-Alpha-07-2016.zip)) comprenant
	* un fichier README.txt (version [HTML](/ressources/API-Alpha/Readme)),
	* le fichier de licence Vitam LICENCE.txt (version [HTML](/ressources/API-Alpha/LICENCE)),
	* un ensemble exécutable avec une JVM 8 (autour d'un serveur jetty) qui expose :
		* la documentation html des API Vitam (pages statiques reprises ci-dessus)
		* l'outil RAML Console permettant de manière dynamique de visualiser la documentation RAML et de faire des tests ([https://github.com/mulesoft/api-console](https://github.com/mulesoft/api-console))
		* les Javadoc de quelques modules Vitam (query-builder, ingest.client, access.client, logbook.client)
		* les points d'entrée REST des API externes de Access (units et objects), de Logbook (operation et lifecycle) et d'Ingest en mode "bouchonné" c'est à dire que les réponses renvoyées par le serveur sont correctes vis à vis de la documentation de l'API mais il s'agit de "fausses" données puisqu'il n'y a pas d'implémentation du back-office Vitam derrière.
	* des exemples de code Java pour l'utilisation des clients Access, Logbook et Ingest
	* des exemples de requêtes CURL vers les APIs Access et Logbook