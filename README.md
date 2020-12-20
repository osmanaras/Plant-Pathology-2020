# Plant-Pathology-2020

Kaggle competition : https://www.kaggle.com/c/plant-pathology-2020-fgvc7/overview

# Objectif :

L'objectuf du compétition est de classifier du les feuilles de plantes selon si il sont saines, rouillés, sèches ou malades.La metric qui doit être utilisr est le AUC-ROC curve. le ROC c'est la courbe du modele qui represente le true positif rate sur le false positif rate et l'auc c'est l'aire sous cette courbe. Plus l'auc est est proche de 1 plus notre modèle classera bien les feuilles.

# Data 
Il ya quelques problèmes dans le dataset. Certains ligne du train set son tirer d'un même image mais labeliser differemment ( exemple Train_379 et Train_1173 ). Un autre problème est le fait qu'il y ait peu de data.

# Solution

## 1- Preprocessing
  Pour obtenir plus de data on va créer de nouvelle image à partir des existants. On va faire ce qu'on appele du Data enhancement. On prend une image est on modifie par exemple la   luminosité, le contraste, etc. En plus d'enrichir le dataset, elle permet aussi au modèle de ne pas trop se spécifier et donc de pour géneraliser. Ce qui va permet d'obtenir de   bon resultat.

## 2 - Model 
  Ici on a utilisé le méthode de knowledge distillation. Cette méthode consiste a utilise les poids(weight) d'un gros modèle entrainner sur un petit modèle. Cela permet de faire   un "transfert de connaissance". Pour cela on va utilise le modèle pré-entrainer **seresnextnet50**. 



***Source***:
- https://www.kaggle.com/c/plant-pathology-2020-fgvc7/discussion/154056 
- https://github.com/alipay/cvpr2020-plant-pathology/tree/9756789b9fa684425064968f497ea630106efca0
