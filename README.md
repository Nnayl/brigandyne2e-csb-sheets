# Brigandyne 2 - CSB - Feuilles de Personnages

Dans l'attente du système de jeu Brigandyne 2 pour Foundry VTT, ce module permet d'intégrer au système de jeu **Custom System Builder** (CSB) les feuilles de PJ et PNJ pour le JDR Brigandyne 2 ainsi que les templates nécessaires à la création d'objets.

## Index

- [1. Dépendance](#1-Dépendance)
- [2. Installation](#2-Installation)
  - [2.1 Manuelle](#21-manuelle)
- [3. Comment utiliser ce module ?](#3-comment-utiliser-ce-module-)
  - [3.1 Introduction](#31-introduction)
  - [3.2 Contenu](#32-contenu)
  - [3.3 Récupérer les templates](#33-récupérer-les-templates)
  - [3.4 Configuration](#34-configuration)
  - [3.5 Créer un acteur](#35-créer-un-acteur)
  - [3.6 Créer un onjet](#36-créer-un-objet)
  - [3.7 Les Objets Préfabriqués](#37-les-objets-préfabriqués)
  - [3.8 Fonctionnent des fiches](#38-fonctionnement-des-fiches)
- [4. Feuille PJ](#4-feuille-pj)
  - [4.1 Information générales](#41-informations-générales)
  - [4.2 Handicaps](#42-handicaps)
  - [4.3 Atouts](#43-atouts)
  - [4.4 Equipements](#44-equipements)
  - [4.5 Grimoire](#45-grimoire)
  - [4.6 Péripéties](#46-péripéties)
  - [4.7 Biographie](#47-biographie)
  - [4.8 MJ](#48-mj)
- [5. Feuille PNJ](#5-feuille-pnj)
- [6. Les jets de dés](#6-les-jets-de-dés)
  - [6.1 Résultat de compétence](#61-résultat-de-compétence)
  - [6.2 Résultat de combat](#62-résultat-de-combat)
  - [6.3 Résultat de magie](#63-résultat-de-magie)
  - [6.4 Objets liés](#64-objets-liés)
- [7. Automatisation](#7-automatisation)
  - [7.1 Paramétrage "Item Modifiers"](#71-paramétrage-item-modifiers)
  - [7.2 La fenêtre "Configure Modifiers"](#72-la-fenêtre-configure-modifiers)
  - [7.3 Objets préfabriqués](#73-objets-préfabriqués)
    - [7.3.1 Arme](#731-arme)
    - [7.3.2 Armure](#732-armure)
    - [7.3.3 Consommable](#733-consommable)
    - [7.3.4 Contenant](#734-contenant)
    - [7.3.5 Munition](#735-munition)
    - [7.3.6 Objet divers](#736-objet-divers)
    - [7.3.7 Peuple](#737-peuple)
    - [7.3.8 Vêtement](#738-vêtement)
- [8. Compatibilité](#8-compatibilité)
  - [8.1 Health Estimate](#81-health-estimate)
  - [8.2 Dice So Nice !](#82-dice-so-nice)


## 1. Dépendance

- Système [Custom System Builder](https://gitlab.com/custom-system-builder/custom-system-builder/-/tree/main)
- Module [Compendium Folder](https://github.com/earlSt1/vtt-compendium-folders)

## 2. Installation

#### 2.1 Manuelle

A partir du manifeste JSON https://raw.githubusercontent.com/Nnayl/brigandyne2e-csb-sheets/master/module.json à renseigner directement dans l'URL du Manifest de l'interface d'installation de module dans Foundry VTT.

<p align="center"><img src="https://github.com/Nnayl/brigandyne2e-csb-sheets/blob/media/url-du-manifest.jpg" width="400"></p>

## 3. Comment utiliser ce module ?

#### 3.1 Introduction

Le système **Custom System Builder** permet de créer des modèles (templates) d'acteurs et d'objets. A travers cette fonctionnalité vous trouverez dans ce module des Templates pour créer : 
- Vos feuilles de PJ et de PNJ
- Les objets (équipements, atouts, sorts, etc...) qui pourront être rattachés aux PJ

Les Templates ne doivent pas être utilisés comme tel, il sèrvent à générer de nouveau acteurs ou obets.

Vous y trouverez aussi des objets préfabriqués qui reposent sur les Templates mentionnés ci-dessus et qui possèdent déjà les formules permettant d'exploiter le système d'automatisation des valeurs calculées. Il est conseillé de créer votre contenu à partir de ces objets en les duplicant, notamment pour l'équipement.

#### 3.2 Contenu

Le module contient deux compendiums (Actors Templates et Item Templates)

- **Actors Templates** contient deux acteurs (PJ Template et PNJ Template) sur lesquelles le système va s'appuyer pour générer les fiches de personnage joueur ou non-joueur. Ces fiches ne doivent pas être utilisées en tant que tel.
- **Items Templates** contient huit objets qui serviront à générer votre équipement, vos sort et différents éléments de jeu.

#### 3.3 Récupérer les Templates

Le module utilise **Compendium Folder** pour organiser les différents templates dans des dossiers. Lorsque vous récupérez le contenu des compendiums, veillez à utiliser la fonctionnalité d'import de **Compendium Folder** et assurez vous que les cases "Merge by name" et "Keep ID" soient cochées.

#### 3.4 Configuration

Avant toute chose, après avoir créé votre partie avec le système de jeu **Custom System Builder** et activé le module **Bigandyne 2 - CSB - Feuilles de Personnages**, il est nécessaire d'apporter quelques éléments à la configuration de la partie.

Dans "Configuration des options de la partie" > "Custom System Builder" il faut renseigner dans les champs :
- Initiative Formula : char_init
- CSS Style file : modules\brigandyne2e-csb-sheets\brigandyne2-sheets.css (à saisir à la main, l'explorateur de fichier de Foundry VTT ne prend pas en charge les CSS)
- Roll Icons : dice-d20

<p align="center"><img src="../media/csb-config.jpg" height="200"></p>

#### 3.5 Créer un acteur

Lorsque vous souhaitez créer un nouvel acteur, dans la fenêtre "Créer un acteur" il faut sélectionner le type "character". Cela génère une nouvelle fiche vierge dans laquelle il faut spécifier le Template à utiliser (PJ Template ou PNJ Template), puis cliquez sur le bouton de rafraichissement. Une fois fait, la nouvelle fiche est prête à être utilisée.

<p align="center"><img src="../media/new-actor.jpg" height="150"><img src="../media/use-template.jpg" height="150"></p>

**Note** : Le champ Template n'est disponible que pour le MJ. Lorsque le Template d'origine est modifié il est nécessaire de rafraichir le Template sélectionné afin d'apporter les modifications sur la fiche.

#### 3.6 Créer un objet

Même procédure que la création d'un acteur, à la différence que le type à sélectionner est "equippableItem".

#### 3.7 Les objets préfabriqués

Pour facilité l'usage du module et permettre un bon fonctionnement de l'automatisation des valeurs calculées de la fiche de personnage en fonction des objets présents sur celle-ci, des objets préfabriqués sont disponibles. Ils embarquent l'ensemble des paramètrages nécessaire à l'automatisation. Plus de détail plus loin.

#### 3.8 Fonctionnement des fiches

Les fiches, qu'elles soient des acteurs ou des objets, sont composées des mêmes éléments :
- des champs de saisie qui permettent d'enregistrer les valeurs souhaitées
- des champs non modifiables qui contiennent des valeurs calculées (les points de vitalité, de sang-froid, etc...)
- des listes qui acceptent des objets créés à partir des Templates prédéfinis (La liste des Spécialités qui acceptent uniquement les objets créés avec le Template Spécialité, etc...)
- des symboles de D20 de couleur rouge qui permettent d'effectuer des jets et d'afficher le résultat dans les messages.

## 4. Feuille PJ

La feuille de personnage est consitituée de 8 onglets. (Informations Génrales, Handicaps, Atouts, Equipements, Magie, Péripéties, Biographie, MJ).

#### 4.1 Informations Générales

On y retrouve la liste des compétences, les attributs secondaires, la monnaie du personnage et un récapitulatif des armes et protections équipées ainsi que les atouts disponibles.

<p align="center"><img src="../media/pj-sheet-1.jpg" width="400"></p>

#### 4.2 Handicaps

Liste les handicaps dont peut souffrir un personnage. Affamé, Assoifé, Démoralisé et Intimidé modifient automatiquement les dégats des armes de corps à corps et de tir, mais pas ceux de magie.

**A noter** : Il n'y a pas d'interaction avec le token pour l'instant. 

<p align="center"><img src="../media/pj-sheet-8.jpg" width="400"></p>

#### 4.3 Atouts

Présente la liste des Spécialités et des Talents du personnage. Chacune des listes acceptent des objets créés à partir des Templates correspondants.

<p align="center"><img src="../media/pj-sheet-2.jpg" width="400"></p>

#### 4.4 Equipements

Présente l'équipements du personnage, catégorisés en 7 listes. (Contenants, Munitions, Armes, Armures, Vêtements, Consommables, Objets Divers)

<p align="center"><img src="../media/pj-sheet-3.jpg" width="400"></p>

#### 4.5 Grimoire

Présente les limites de sorts par jour que le personnage peut lancer ainsi que tours, sortillèges et rituels en sa connaissance.

<p align="center"><img src="../media/pj-sheet-4.jpg" width="400"></p>

#### 4.6 Péripéties

Cet onglet permet de suivre les afflictions dont souffre le personnage, tel que les maladies, les poisons, les séquelles et les troubles mentaux.

<p align="center"><img src="../media/pj-sheet-5.jpg" width="400"></p>

#### 4.7 Biographie

Ici sont compilées les informations correspondant à l'identité du personnage, ses caractéristiques physiques, ses vices & vertues, son expérience.

<p align="center"><img src="../media/pj-sheet-6.jpg" width="400"></p>

#### 4.8 MJ

Cette section est réservé au MJ et lui permet de prendre des notes sur la fiche du personnage.

<p align="center"><img src="../media/pj-sheet-7.jpg" width="400"></p>

## 5. Feuille PNJ

<p align="center"><img src="../media/pnj-sheet.jpg" width="400"></p>

La feuille de personnage non-joueur a été simplifiée au regard de ce qui est disponible dans Brigandyne 2. Elle comprend toutes les informations essentielles nécessaires à son utilisation.

Les compétences, les tactiques, les Spécials et l'équipements sont disponibles dans une liste dynamique. En cliquant sur le "+" il est possible d'y rajouter des éléments.

## 6. Les Jets de dés

Les fiches de PJ et de PNJ contiennent des symboles de D20 qui permettent d'effectuer les jets de compétences depuis les listes de compétences ou de combat depuis l'équipement équipé (uniquement pour les PJ).

**!! ATTENTION !!** - Pour que le symbole du D20 soit visible il faut bien configurer le système, voir Configuration

Lors d'un jet de dés, une fenêtre s'affiche afin d'y renseigner les éventuels modificateurs et avantages/désavantages.

<p align="center"><img src="../media/modif-dialog.jpg" width="200"></p>

#### 6.1 Résultat de Compétence

Le résultat du jet s'affiche dans la liste des messages et présente quelques informations.

- La compétence utilisée
- Le degré de réussite (Echec majeur, Echec, Réussite, Réussite Majeure, Critique, Double critique)
- Le résultat du Jet
- Les chances de réussite, accompagné de la somme des modificateurs entre paranthèses
- Le Résultat des Unités. Entre paranthèse est disponible le résultat de l'explosion en cas de critique

<p align="center"><img src="../media/skill-result.jpg" width="200"></p>

#### 6.2 Résultat de Combat

Les jets de combats présente des informations complémentaires

- Le lien de l'arme utilisée
- Le nom de l'arme
- les dégats de l'arme ainsi qu'entre paranthèse les dégâts calculés (RU + Dégâts Arme)
- L'allonge de l'arme

<p align="center"><img src="../media/fight-result.jpg" width="200"></p>

#### 6.3 Résultat de Magie

Les jets de magie, comme pour le combat, apporte le lien du sort utilisé ainsi que la description de ce dernier.

<p align="center"><img src="../media/magic-result.jpg" width="200"></p>

#### 6.4 Objets liés

Pour que les liens fonctionnent correctement dans les messages, il est nécessaire que les objets soient disponibles dans l'onglet "Objets" de la partie Foundry VTT.

## 7 Automatisation

Certaines valeures de la fiche de personnage sont calculées automatiquement. C'est notamment le cas pour :
- La vitalité
- Le sang-froid
- L'initiative
- La protection
- La valeur actuelle d'une compétence
- L'encombrement

Pour que cela soit possible les objets qui sont déposés dans une fiche de personnage doivent contenir certains paramètres spécifiques que l'on définit à l'aide de l'Item Modifiers présent sur chaque objet.

#### 7.1 Paramétrage "Item Modifiers"

Chaque fiche objet possède un bouton "Item Modifiers", hérité du système **Custom System Builder**, qui permet de paramétrer des formules qui vont impacter directement les données des fiches de personnage sur lesquelles les objets seront déposés.

**Note** : Les limitations actuelles du système **Custom System Builder** font que les Items Modifiers ne sont accessibles que sur les fiches d'objets et non directement sur le Template. Ce qui implique qu'il est nécessaire de les paramétrer sur chaque objet. 

<p align="center"><img src="../media/item-modifiers.jpg" height="200"></p>

Vous trouverez plus loin le détail des paramètres par type d'objet.

Dans tous les cas, il est conseillé d'utiliser les objets préfabriqués qui sont disponibles dans le compendium Template. Ils embarquent déjà tout le paramétrage de l'"Item Modifiers" qui est nécessaire pour l'automatisation des valeurs calculées de la fiche de personnage.

#### 7.2 La fenêtre "Configure Modifiers"

Il s'agit d'un tableau d'éléments dont chaque élément contient quatre propriétés.
- Prio. : Correspond à l'ordre de priorité de chargement
- Key : Fait référence à la clé de l'élément à modifier sur la fiche de personnage
- Op. : Indique quel opérateur utiliser
- Value formula : Représente la formule qui sera évaluée

<p align="center"><img src="../media/set-item-modifiers.jpg" width="250"></p>

#### 7.3 Objets préfabriqués

Il existe 8 objets préfabriqués différents dont les paramètres Item Modifiers sont déjà renseignés. Voici la liste avec leurs implications :
- Arme
  - Encombrement, Initiative 
- Armure
  - Encombrement, Initiative, Protection, Mouvement
- Consommable
  - Encombrement
- Contenant
  - Encombrement, Extension d'encombrement
- Munition
  - Encombrement
- Objet Divers
  - Encombrement
- Peuple
  - Vitalité, Sang-froid, Destin
- Vêtement
  - Encombrement

  Ci-dessous le détails des paramètres pour chacun des objets préfabriqués. **Reservé aux utilisateurs avertis**.

##### 7.3.1 Arme

Les armes vont impacter l'encombrement général, l'encombrement d'objets équipés et l'initiative.

- Paramètres
  - current_enc       +   ```${item_enc}$```
  - char_init         +   ```${${item_equiped ? item_init : 0}$}$```
  - current_hard_enc  +   ```${item_equiped ? item_enc : 0}$```

##### 7.3.2 Armure

Les armures vont impacter l'encombrement générale, l'encombrement d'objets équipés, la protection, l'initiative et le mouvement.

- Paramètres
  - current_enc       +   ```${item_enc}$```
  - char_init         +   ```${${item_equiped ? item_init : 0}$}$```
  - current_hard_enc  +   ```${item_equiped ? item_enc : 0}$```
  - current_armor     +   ```${${item_equiped ? armor_value : 0}$}$```
  - skill_end_mou     +   ```${${item_equiped ? item_mou : 0}$}$```

##### 7.3.3 Consommable

Les consommables vont impacter l'encombrement général en fonction de la quantité.

- Paramètres
  - current_enc       +   ```${item_enc * item_count}$```

##### 7.3.4 Contenant

Les contenants possède une case à cocher "Enc. Relatif ?" uniquement visible par le MJ. Elle permet d'indiquer si l'objet prend une valeur à 0 lorsqu'il est équipé.

Un contenant équipé et qui n'a pas pas un "Enc. Relatif ?" compte dans la charge équipé. Ce type de profil de contenant représente les objets qui peuvent en contenir d'autres mais qui restent malgré tout encombrant lorsque équipés.

Les contenants vont impacter l'encombrement générale, l'encombrement équipé ainsi que permettre l'extension du maximum de l'encombrement général.

- Paramètres
  - current_enc       +   ```${item_enc_rel ? (item_equiped ? 0 : item_enc) : item_enc}$```
  - max_enc           +   ```${item_enc_rel ? (item_equiped ? item_enc_bonus : 0) : item_enc_bonus}$```
  - current_hard_enc  +   ```${item_enc_rel ? 0 : (item_equiped ? item_enc : 0)}$$```

##### 7.3.5 Munition

Les munitions vont impacter l'encombrement général en fonction de la quantité.

- Paramètres
  - current_enc       +   ```${item_enc * item_count}$```

##### 7.3.6 Objet Divers

Les objets divers vont impacter l'encombrement général en fonction de la quantité.

- Paramètres
  - current_enc       +   ```${item_enc * item_count}$```

##### 7.3.7 Peuple

Les peuples vont impacter la vitalité, le sang-froid et le destin.

- Paramètres
  - max_hp       +   ```${bonus_hp}$```
  - max_sf       +   ```${bonus_sf}$```
  - max_fate     +   ```${nb_fate}$```

##### 7.3.8 Vêtement

Les vêtement vont impacter l'encombrement général en fonction de la quantité. Si l'objet est équipé sont encombrement tombe à 0.

- Paramètres
  - current_enc       +   ```${item_equiped ? item_enc * (item_count - 1) : item_enc * item_count}$```

## 8. Compatibilité

#### 8.1 Health Estimate

Afin que le système puisse effectuer correctement l'estimation de la vie du token, il est nécessaire de paramétrer Health Estimate comme suit :

- Chemin des données de Points de vie : actor.system.attributeBar.current_hp

#### 8.2 Dice so Nice !

Le système est nativement compatible avec ce module, toute fois (pour une raison encore indéterminée) le module prend en compte le dé d'explosion même si il n'ya à pas de critique. Cela génère pour effet de bord de voir 3 dés 10 à l'écran au lieu de 2.