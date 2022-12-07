# Brigandyne 2 - CSB - Feuilles de Personnages

Ce module a pour objectif de permettre d'intégrer au système de jeu **Custom System Builder** (CSB) les feuilles de PJ et PNJ pour le JDR Brigandyne 2 ainsi que les templates nécessaires à la création d'objets, ceci en attendant que le Système Brigandyne 2 soit intégré et disponible sur Foundry VTT.

## Index

[[_TOC_]]

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

#### Récupérer les Templates

Le module utilise **Compendium Folder** pour organiser les différents templates dans des dossiers. Lorsque vous récupérez le contenu des compendiums, veillez à utiliser la fonctionnalité d'import de **Compendium Folder** et assurez vous que les cases "Merge by name" et "Keep ID" soient cochées.

#### Configuration

Avant toute chose, après avoir créé votre partie avec le système de jeu **Custom System Builder** et activé le module **Bigandyne 2 - CSB - Feuilles de Personnages**, il est nécessaire d'apporter quelques éléments à la configuration de la partie.

Dans "Configuration des options de la partie" > "Custom System Builder" il faut renseigner dans les champs :
- Initiative Formula : char_init
- CSS Style file : modules\brigandyne2e-csb-sheets\brigandyne2-sheets.css (à saisir à la main, l'explorateur de fichier de Foundry VTT ne prend pas en charge les CSS)
- Roll Icons : dice-d20

<p align="center"><img src="../media/csb-config.jpg" height="200"></p>

#### Créer un acteur

Lorsque vous souhaitez créer un nouvel acteur, dans la fenêtre "Créer un acteur" il faut sélectionner le type "character". Cela génère une nouvelle fiche vierge dans laquelle il faut spécifier le Template à utiliser (PJ Template ou PNJ Template), puis cliquez sur le bouton de rafraichissement. Une fois fait, la nouvelle fiche est prête à être utilisée.

<p align="center"><img src="../media/new-actor.jpg" height="150"><img src="../media/use-template.jpg" height="150"></p>

**Note** : Le champ Template n'est disponible que pour le MJ. Lorsque le Template d'origine est modifié il est nécessaire de rafraichir le Template sélectionné afin d'apporter les modifications sur la fiche.

#### Créer un objet

Même procédure que la création d'un acteur, à la différence que le type à sélectionner est "equippableItem".

#### Fonctionnement des fiches

Les fiches, qu'elles soient des acteurs ou des objets, sont composées des mêmes éléments :
- des champs de saisie qui permettent d'enregistrer les valeurs souhaitées
- des champs non modifiables qui contiennent des valeurs calculées (les points de vitalité, de sang-froid, etc...)
- des listes qui acceptent des objets créés à partir des Templates prédéfinis (La liste des Spécialités qui acceptent uniquement les objets créés avec le Template Spécialité, etc...)
- des symboles de D20 de couleur rouge qui permettent d'effectuer des jets et d'afficher le résultat dans les messages.

## 1. Feuille PJ

<p align="center"><img src="../media/pj-sheet.jpg" width="400"></p>

La feuille de personnage est consitituée de 6 onglets. (Informations Génrales, Atouts, Equipements, Magie, Péripéties, Biographie).

#### Informations Générales

On y retrouve la liste des compétences, les attributs secondaires, la monnaie du personnage et un récapitulatif des armes et protections équipées ainsi que les atouts disponibles.

#### Atouts

Présente la liste des Spécialités et des Talents du personnage. Chacune des listes acceptent des objets créés à partir des Templates correspondants.

#### Equipements

Présente l'équipements du personnage, catégorisés en quatre liste. (Armes, Armures, Vêtements, Consommables, Objets Divers)

#### Magie

Présente les limites de sorts par jour que le personnage peut lancer ainsi que tours, sortillèges et rituels en sa connaissance.

#### Péripéties

Cet onglet permet de suivre les afflictions dont souffre le personnage, tel que les maladies, les poisons, les séquelles et les troubles mentaux.

#### Biographie

Ici sont compilées les informations correspondant à l'identité du personnage, ses caractéristiques physiques, ses vices & vertues, son expérience.

## Feuille PNJ

<p align="center"><img src="../media/pnj-sheet.jpg" width="400"></p>

La feuille de personnage non-joueur a été simplifié au regard de ce qui est disponible dans Brigandyne 2. Elle comprend toutes les informations essentielles nécessaires à son utilisation.

Les compétences, les tactiques, les Spécials et l'équipements sont disponibles dans une liste dynamique. En cliquant sur le "+" il est possible d'y rajouter des éléments.

## Les Jets de dés

Les fiches de PJ et de PNJ contiennent des symboles de D20 qui permettent d'effectuer les jets de compétences depuis les listes de compétences ou de combat depuis l'équipement équipé (uniquement pour les PJ).

**!! ATTENTION !!** - Pour que le symbole du D20 soit visible il faut bien configurer le système, voir Configuration

Lors d'un jet de dés, une fenêtre s'affiche afin d'y renseigner les éventuels modificateurs et avantages/désavantages.

<p align="center"><img src="../media/modif-dialog.jpg" width="200"></p>

#### Résultat de Compétence

Le résultat du jet s'affiche dans la liste des messages et présente quelques informations.

- La compétence utilisée
- Le degré de réussite (Echec majeur, Echec, Réussite, Réussite Majeure, Critique, Double critique)
- Le résultat du Jet
- Les chances de réussite, accompagné de la somme des modificateurs entre paranthèses
- Le Résultat des Unités. Entre paranthèse est disponible le résultat de l'explosion en cas de critique

<p align="center"><img src="../media/skill-result.jpg" width="200"></p>

#### Résultat de Combat

Les jets de combats présente des informations complémentaires

- Le lien de l'arme utilisée
- Le nom de l'arme
- les dégats de l'arme ainsi qu'entre paranthèse les dégâts calculés (RU + Dégâts Arme)
- L'allonge de l'arme

<p align="center"><img src="../media/fight-result.jpg" width="200"></p>

#### Résultat de Magie

Les jets de magie, comme pour le combat, apporte le lien du sort utilisé ainsi que la description de ce dernier.

<p align="center"><img src="../magic-result.jpg" width="200"></p>

#### Objets liés

Pour que les liens fonctionnent correctement dans les messages, il est nécessaire que les objets soient disponibles dans l'onglet "Objets" de la partie Foundry VTT.

## Objets et "Item Modifiers"

Chaque fiche objet possède un bouton "Item Modifiers", hérité du système **Custom System Builder**, qui permet de renseigner des formules qui impacteront la fiche personnage en fonction des éléments présents sur la fiche objet. Voici comment les utiliser.

<p align="center"><img src="../media/item-modifiers.jpg" height="200"></p>

#### La fenêtre Configure Modifiers

Il s'agit d'un tableau d'éléments dont chaque élément contient quatre propriétés.
- Prio. : Correspond à l'ordre de priorité de chargement
- Key : Fait référence à la clé de l'élément à modifier sur la fiche de personnage
- Op. : Indique quel opérateur utiliser
- Value formula : Représente la formule qui sera exécutée

Ci-après les propriétés à remplir. [X] doit être remplacé par la valeur que vous souhaitez appliquer, elle peut être négative.

#### L'encombrement

Peut-être appliqué sur tous les objets créés à partir des Templates Armes, Armures et Objets.

- Encombrement
  - Key : current_enc
  - Op. : +
  - Formula : ```${item_enc}$```

#### Les Armures

Avec le objets armures il est possible de calculer directement la protection d'un personnage, le malus d'initiative et de Mouvement.

- Protection
  - Key : current_armor
  - Op. : +
  - Formula : ```${item_equiped ? armor_value : 0}$```
- Initiative
  - Key : char_init
  - Op. : +
  - Formula : ```${item_equiped ? [X] : 0}$```
- Mouvement
  - Key : skill_end_mou
  - Op. : +
  - Formula : ```${item_equiped ? [X] : 0}$```

<p align="center"><img src="../media/set-item-modifiers.jpg" width="250"></p>

## Limitation

Du fait qu'un système est en cours de développement pour Brigandyne 2 je n'ai pas cherché à passer plus de temps sur les automatisations. Mis à part quelques valeurs calculées, il n'y a pas d'interaction dynamique entre les résultats de dés et les attributs dans les fiches. 

L'objectif n'est pas de créer un système avec tout son lot d'automatisation, mais simplement des ressources permettant de jouer à Brigandyne 2 sur Foundry VTT.

## Compatibilité

#### Health Estimate

Afin que le système puisse effectuer correctement l'estimation de la vie du token, il est nécessaire de paramétrer Health Estimate comme suit :

- Chemin des données de Points de vie : actor.system.attributeBar.current_hp

#### Dice so Nice !

Le système est nativement compatible avec ce module, toute fois (pour une raison encore indéterminée) le module prend en compte le dé d'explosion même si il n'ya à pas de critique. Cela génère pour effet de bord de voir 3 dés 10 à l'écran au lieu de 2.