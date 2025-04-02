# Comment spécialiser DINOv2 pour l'astronomie ?

Ce projet contient le code Python de reproduction des figures associé à l'article :

> Le Lain, M., Lefèvre, S. (2025). "*Comment spécialiser DINOv2 pour l'astronomie ?*". Soumis au colloque [GRETSI 2025](https://gretsi.fr/colloque2025/) (En revision).

## Installation

### Cloner le dépôt
Pour cloner le dépôt, exécutez la commande suivante dans votre terminal :
```sh
git clone https://github.com/matthieulel/finetune_dinov2_astronomy.git

cd /finetune_dinov2_astronomy
```

### Installation avec Conda (recommandé)
Créer un environnement Conda et installer les dépendances à partir du fichier `environment.yml` fourni.

1. Assurez-vous d'avoir Conda installé. Vous pouvez vérifier en exécutant :
   ```sh
   conda --version
   ```
2. Créez un nouvel environnement Conda à partir du fichier `environment.yml` :
   ```sh
    conda env create -f environment.yml
    ```
3. Activez l'environnement :
4. ```sh
    conda activate dinov2
    ```



### Installation avec pip
La liste des dépendances est fournie dans le fichier `requirements.txt`. Il est recommandé d'utiliser un environnement virtuel.

Pour installer les dépendances, vous pouvez utiliser `pip` avec le fichier `requirements.txt` fourni.

1. Assurez-vous d'avoir Python et pip installés, nous recommandons d'utiliser Python 3.11 ou une version ultérieure. 
Vérification de la version de Python et pip :
   ```sh
   python3 --version
   pip --version
   ```

1. Créez et activez un environnement virtuel :
   ```sh
    python3 -m venv envdinov2
    source envdinov2/bin/activate  
    ```

2. Installer les dépendances à partir de `requirements.txt` :
   ```sh
   pip install -r requirements.txt
   ```


### Installer et activer CUDA
(optionnel mais recommandé pour obtenir le même temps d'exécution qu'indiqué dans l'issue)

Pour utiliser CUDA avec PyTorch, vous devez installer la version de PyTorch compatible avec votre version de CUDA. Vous pouvez le faire en suivant les instructions sur le site officiel de PyTorch : https://pytorch.org/get-started/locally/
Assurez-vous de choisir la version de CUDA qui correspond à votre configuration matérielle et logicielle.

### Vérification de l'installation de CUDA
Pour vérifier que PyTorch et CUDA sont correctement installés, vous pouvez exécuter le code suivant dans un terminal Python :
```python
import torch
print("CUDA available:", torch.cuda.is_available())
print("CUDA version:", torch.version.cuda)
print("PyTorch version:", torch.__version__)
```


## Utilisation

- Ouvrez les notebooks Jupyter et exécutez les cellules pour reproduire les résultats de l'article.

- Liste des notebooks: 
  - `tsne_fig3_fig5.ipynb` : Images t-SNE pour la figure 3 et la figure 5
  - `matriceFig4_Tab2Dinov2.ipynb` : Matrice de confusion pour la figure 2 et la colonne DINOv2 du tableau 2
  - `tsne_mnist_fig6.ipynb` : Images t-SNE pour la figure 6