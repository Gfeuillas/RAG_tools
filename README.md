# RAG francophone (notebook)

Ce dépôt contient un notebook minimal pour tester une chaîne Retrieval-Augmented Generation (RAG) en français avec LangChain et des modèles gratuits de Hugging Face.

## Fichiers principaux
- `rag_fr_demo.ipynb` : le notebook prêt à exécuter.
- `requirements.txt` : dépendances Python.
- `data/source.txt` : fichier texte initial utilisé pour alimenter l'index vectoriel.

## Variables et paramètres à ajuster
Modifiez ces variables dans la première cellule du notebook :

- `DATA_PATH` : chemin vers le fichier texte à indexer (par défaut `data/source.txt`).
- `EMBEDDING_MODEL` : identifiant Hugging Face de l'encodeur multilingue pour les embeddings (par défaut `sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2`).
- `GENERATION_MODEL` : identifiant Hugging Face du modèle de génération (par défaut `google/flan-t5-small`, gratuit et multilingue). Remplacez-le par un modèle francophone plus grand si vous disposez des ressources nécessaires.
- `HF_HOME` : dossier de cache pour les poids téléchargés. Laisser par défaut ou remplacer par votre emplacement préféré.

> Si vous utilisez un modèle nécessitant un jeton d'accès, exportez `HUGGINGFACEHUB_API_TOKEN` dans votre environnement avant d'ouvrir le notebook.

## Prérequis et lancement
1. Assurez-vous d'avoir Python 3.10+.
2. Installez les dépendances :
   ```bash
   pip install -r requirements.txt
   ```
3. Remplacez le contenu de `data/source.txt` par votre propre texte francophone.
4. Ouvrez le notebook et exécutez les cellules dans l'ordre pour créer l'index FAISS et lancer une requête RAG :
   ```bash
   jupyter notebook rag_fr_demo.ipynb
   ```

Les téléchargements de modèles se font depuis Hugging Face en utilisant uniquement des ressources gratuites.
