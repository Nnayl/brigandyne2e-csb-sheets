# Brigandyne 2 - CSB - Feuilles de Personnages

Ce module à pour objectif de permettre d'intégrer au système de jeu Custom System Builder (CSB) les feuilles de PJ et PNJ pour le JDR Brigandyne 2 ainsi que les templates nécessaires à la création d'objets, en attendant que le Système Brigandyne 2 soit intégré et disponible sur Foundry VTT.

## Dépendance

- Système [Custom System Builder](https://gitlab.com/custom-system-builder/custom-system-builder/-/tree/main)
- Module [Compendium Folder](https://github.com/earlSt1/vtt-compendium-folders)

## Installation

#### Manuelle

A partir du manifeste JSON https://raw.githubusercontent.com/Nnayl/brigandyne2e-csb-sheets/master/module.json à renseigner directement dans l'URL du Manifest de l'interface d'installation de module dans Foundry VTT.

<p align="center"><img src="https://github.com/Nnayl/brigandyne2e-csb-sheets/blob/media/url-du-manifest.jpg" width="400"></p>

## Comment utiliser ce module ?

#### Introduction

Le système **Custom System Builder** permet de créer des modèles (templates) d'acteurs et d'objets. A travers cette fonctionnalité vous trouverez dans ce module des Templates pour créer : 
- Vos feuilles de PJ et de PNJ
- Les objets (équipements, atouts, sorts, etc...) qui pourront être rattachés aux PJ

Les Templates ne doivent pas être utilisés comme tel, il sèrvent à générer de nouveau acteurs ou obets.

#### Contenu

Le module contient deux compendiums (Actors Templates et Item Templates)

- **Actors Templates** contient deux acteurs (PJ Template et PNJ Template) sur lesquelles le système va s'appuyer pour générer les fiches de personnage joueur ou non-joueur. Ces fiches ne doivent pas être utilisées en tant que tel.
- **Items Templates** contient huit objets qui serviront à générer votre équipement, vos sort et différents éléments de jeu.

#### Configuration

Avant toute chose, après avoir créé votre partie avec le système de jeu**Custom System Builder**, il est nécessaire d'apporter quelques éléments à la configuration de ce dernier.

Dans "Configuration des options de la partie" > "Custom System Builder" il faut renseigner dans les champs :
- CSS Style file : modules\brigandyne2e-csb-sheets\brigandyne2-sheets.css
- Roll Icons : dice-d20

<p align="center"><img src="https://github.com/Nnayl/brigandyne2e-csb-sheets/blob/media/csb-config.jpg" height="200"></p>

#### Créer un acteur

Lorsque vous souhaitez créer un nouvel acteur, dans la fenêtre "Créer un acteur" il faut sélectionner le type "character". Cela génère une nouvelle fiche vierge dans laquelle il faut spécifier le Template à utiliser (PJ Template ou PNJ Template), puis cliquez sur le bouton de rafraichissement. Une fois fait, la nouvelle fiche est prête à être utilisée.

<p align="center"><img src="https://github.com/Nnayl/brigandyne2e-csb-sheets/blob/media/new-actor.jpg" height="150"><img src="https://github.com/Nnayl/brigandyne2e-csb-sheets/blob/media/use-template.jpg" height="150"></p>

**Note** : que le champ Template n'est disponible que pour le MJ et que lorsque le Template d'origine est modifié, il est nécessaire de rafraichir le Template sélectionné afin d'apporter les modifications sur la fiche.

#### Créer un objet

Même procédure que la création d'un acteur, à la différence que le type à sélectionner est "equippableItem".

#### Fonctionnement des fiches

Les fiches, qu'elles soient des acteurs ou des objets, sont composées de différents éléments :
- des champs de saisie qui permettent d'enregistrer les valeurs souhaitées
- des champs non modifiable qui contiennent des valeurs calculées (les points de vitalité, de sang-froid, etc...)
- des listes qui acceptent des objets créés à partir des Templates prédéfinis (La liste des Spécialités qui acceptent les objets créés avec le Template Spécialité, etc...)
- des symboles de D20 de couleur rouge qui permettent d'effectuer des jets et d'afficher le résultat dans la liste des messages.

## 1. Feuille PJ

<p align="center"><img src="https://github.com/Nnayl/brigandyne2e-csb-sheets/blob/media/pj-sheet.jpg" width="400"></p>

La feuille de personnage est consitituée de 6 onglets. (Informations Génrales, Atouts, Equipements, Magie, Péripéties, Biographie).

#### Informations Générales

On y retrouve la liste des compétences, les attributs secondaires, la monnaie du personnage et un récapitulatif des armes et protections équipées ainsi que les atouts disponibles.

#### Atouts

Présente la liste des Spécialités et des Talents du personnage. Chacune des listes acceptent des objets créés à partir des Templates correspondants.

#### Equipements

Présente l'équipement du personnage, catégorisé en quatre liste. (Armes, Armures, Vêtements, Consommables, Objets Divers)

#### Magie

Présente les limites de sorts par jour que le personnage peut lancer ainsi que tours, sortillèges et rituels en sa connaissance.

#### Péripéties

Cet onglet permet de suivre les afflictions dont souffre le personnage, tel que les maladies, les poisons, les séquelles et les troubles mentaux.

#### Biographie

Ici sont compilées les informations correspondant à l'identité du personnage, ses caractéristiques physiques, ses vices & vertues, son expérience.

## Feuille PNJ

<p align="center"><img src="https://github.com/Nnayl/brigandyne2e-csb-sheets/blob/media/pnj-sheet.jpg" width="400"></p>

La feuille de personnage non-joueur a été simplifié au regard de ce qui est disponible dans Brigandyne 2. Elle comprend toutes les informations essentielles nécessaire à son utilisation.

Les compétences, les tactiques, les Spécials et l'équipements sont disponibles dans une liste dynamique. En cliquant sur le "+" il est possible d'y rajouter des éléments.

## Les Jets de dés

Les fiches de PJ et de PNJ contiennent des symboles de D20 qui permettent d'effectuer les jets de compétences depuis les listes de compétences ou de combat depuis l'équipement équipé (uniquement pour les PJ).

**!! ATTENTION !!** - Pour que le symbole du D20 soit visible il faut bien configurer le système, voir Configuration

Lors d'un jet de dé, une fenêtre s'affiche afin d'y renseigner les éventuels modificateurs et avantages/désavantages.

<p align="center"><img src="https://github.com/Nnayl/brigandyne2e-csb-sheets/blob/media/modif-dialog.jpg" width="200"></p>

#### Résultat de Compétence

Le résultat du jet s'affiche dans la liste des messages et présente quelques informations.

- La compétence utilisée
- Le degré de réussite (Echec majeur, Echec, Réussite, Réussite Majeure, Critique, Double critique)
- Le résultat du Jet
- Les chances de réussite, accompagné de la somme des modificateurs entre paranthèses
- Le Résultat des Unités. Entre paranthèse est disponible le résultat de l'explosion en cas de critique

<p align="center"><img src="https://github.com/Nnayl/brigandyne2e-csb-sheets/blob/media/skill-result.jpg" width="200"></p>

#### Résultat de Combat

Les jets de combats présente des informations complémentaires

- Le lien de l'arme utilisée
- Le nom de l'arme
- les dégats de l'arme ainsi qu'entre paranthèse les dégâts calculés (RU + Dégâts Arme)
- L'allonge de l'arme

<p align="center"><img src="https://github.com/Nnayl/brigandyne2e-csb-sheets/blob/media/fight-result.jpg" width="200"></p>

#### Résultat de Magie

Les jets de magie, comme pour le combat, apporte le lien du sort utilisé ainsi que la description de ce dernier.

<p align="center"><img src="https://github.com/Nnayl/brigandyne2e-csb-sheets/blob/media/magic-result.jpg" width="200"></p>

#### Onjets liés

Pour que les liens fonctionnent correctement dans les messages, il est nécessaire que les objets soient disponibles dans l'onglet "Objets" de la partie Foundry VTT.