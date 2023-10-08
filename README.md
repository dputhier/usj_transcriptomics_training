# Bioinformatique pour l’analyse du transcriptome

- Enseignants: 
  - Denis Puthier, PR, Aix-Marseille University, TAGC Inserm 1090, MarMaRa (Marseille Maladie rare Institute), TGML, Marseille, France,
  - Béatrice Loriod, IR, Inserm, TAGC Inserm 1090, TGML, Marseille, France.
- Lieux: Année Universitaire 2023-24 -- Université de Saint-Jérome -- Beyrouth
- Public: Etudiants en Master 
- Thématiques: Approches de séquençage à haut débit – Approches de transcriptomique bulk, single-cell - Transcriptomique spatiale - Structure et Analyse du Génome – Expression des Gènes et Régulation Transcriptionnelles -
Programmation avec R - Développement de chaînes de traitement avec Galaxy.

## Analyse de données RNA-seq bulk

Dans cette session, il s'agit de découvrir l'environnement Galaxy et de l'utiliser pour créer une chaîne de traitement dédiée à l'analyse des données de RNA-seq au format brut (fastq). Nous réaliserons les différentes étapes de traitement jusqu'à l'analyse différentielle (Differential Gene Expression, DEG). Nous profiterons de cette opportunité pour naviguer dans le génome murin et le (re)découvrir à la lumière des résultats de RNA-seq obtenus. Le jeu de données porte sur une lignée de lymphocytes T (P5424) stimulée ou non par PMA et Ionomycine

- [Support](https://docs.google.com/presentation/d/11CZU0mBnmECZR7yMwBFPtK-qGsy4jktjcjB8yociDUw/edit?usp=sharing) (google slides)
- Instructions: Pour pouvoir utiliser les ressources informatiques que nous avons réservées pour vous, chaque étudiant de votre formation devra.
  - Créer un compte sur [https://usegalaxy.fr](https://usegalaxy.fr)
  - Ensuite, visitez ce lien [https://usegalaxy.fr/join-training/usj-master-rnaseq](https://usegalaxy.fr/join-training/usj-master-rnaseq)
  - Après cela, les étudiants pourront utiliser Galaxy comme d'habitude. Tous leurs travaux utiliseront automatiquement les ressources informatiques réservées.

Merci à Thomas Chaussepied et à toute l'équipe de l'IFB.


## Initiation au logiciel R

Pour cette initiation nous allons utiliser la librairie R [rtrainer](https://github.com/dputhier/rtrainer/) (développé par D. Puthier dans le cadre de ce cours). L'ojectif est de proposer une librairie proposant un certain nombre d'exercices interactif en mode "Self-Paced training". 

Nous utiliserons pour ce tutoriel le serveur Jupyter de L'IFB qui propose un accès à RStudio Serveur. Pour installer rtrainer vous devez tout d'abord:

- Vous rendre sur le [serveur Jupyter de l'IFB](https://jupyterhub.cluster.france-bioinformatique.fr/).
- Vous connecter avec les logins qui vous ont été fournis.
- Lancer une machine virtuelle (2Gb RAM, 2 coeurs).
- Lancer une instance de Rstudio.
- Installer la librairie rtrainer:
  
```
    install.packages("devtools")
    devtools::install_github("dputhier/rtrainer")
```

- Lister les tutoriels:

```
library(learnr)
learnr::available_tutorials("rtrainer")
```

- Lancer les tutoriels dans l'ordre avec la commande:

```
learnr::run_tutorial("01_preambules", "rtrainer")
```

Merci à Nicole Charrière et à toute l'équipe de l'IFB.

## Initiation à l'analyse de données de séquençage sur cellules uniques (scRNA-seq)

Pour ce tutoriel, nous réaliserons une analyse guidée, pas à pas, des données PBMC3k proposer par le Satija Lab qui développe le très populaire logiciel Seurat. Ce jeu de données correspond à l'analyse de 3000 PBMC (Peripheral Blood Mononuclear Cells). 

- [Cours théorique](https://docs.google.com/presentation/d/1BkdIjF9mA6caG5v-lBdtriH3VfLpDH8cJq5i6Z4_yKU/edit?usp=sharing).
- [Phase pratique](https://satijalab.org/seurat/articles/pbmc3k_tutorial.html).

## Initiation à l'analyse de données de transcriptomique Spatiale sur technologie Visium (10X Genomics)

L'avènement des technologies de transcriptomique spatiale marque une révolution majeure dans le domaine de la biologie moléculaire et de la génomique. L'objectif principal de ces technologies est de cartographier de manière précise et exhaustive l'expression génique à l'échelle tissulaire, offrant ainsi une description inédite des processus biologiques et des interactions cellulaires au sein de tissus complexes.

L'une des approches commerciales phares est la technologies Visium, développée par 10X Genomics. Celle-ci repose sur le "barre codage" d'ARN à l'aide de spots d'oligonucléotides immobilisés sur une lame de verre, permettant de localiser l'expression de milliers de gènes dans un tissu donné. 

- [Cours théorique](https://docs.google.com/presentation/d/1g80o6T4aSJCwZoHfPaSN807rgN17GzzwhKVsVeT3sJU/edit?usp=sharing).
- [Phase pratique](https://satijalab.org/seurat/articles/spatial_vignette.html).


