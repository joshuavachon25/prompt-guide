# ChatGPT (FR)
## Modèle GPT
- ChatGPT est une interface utilisateur et une configuration pour l'implémentation pour les modèles GPT (GPT 3.5, GPT 4...)
- Le modèle ne fonctionne pas avec des mots, mais avec des tokens
- Le modèle prédit le prochain token, mais en prenant en considération le contexte

### GPT 
- Generative Pre-trained Transformer: Réseau de neuronnes batit sur l'architecture transformer de type Large Language Model (LLM) ou Natural Language Processing (NLP)
- Le transformer met a profit la puissance du calcul en paralèlle des GPU.
- Transformers: Architecture basé sur un article de Google de 2017 (Attention is all you need) ou on enlève l'encodeur pour utiliser le décodeur pour passer des arguments de base
- Les frameworks comme Tensorflow ou Pytorch sont développer en C++ et appel les processus CUDA qui permettent d'utiliser les GPUs
- Réseaux de neuronnes: Gros calcul permettant d'établir des paramètres (éléments liés numériquement) sur plusieurs niveaux.
  - GPT 3: 175 milliards de params
  - GPT 4: + de 1000 milliards de params
- Le modèle est entrainé à partir de:
  - Common Crawl (Ensemble de pages web en 40 langues)
  - Webtext2 (Sites web mentionnés dans des posts Reddit upvotés)
  - Bookcorpus (Peut être)
  - Wikipedia
  - ...

### Tokens
- Le token est un morceau de mot répertorié dans un dictionnaires. Il ne correspond pas à des mots, mais des compositions de caractères.
- Le dictionnaire pour GPT 3.5 et 4 contient plus de 100 000 tokens (Plus il y a de tokens dans le dictionnaire, moins vous utilisez de tokens)
- Les tokens sont représentés par des valeurs numériques
- Pour savoir le nombre de tokens dans un texte, utiliser [GPT Tokenizer Playground](https://gpt-tokenizer.dev)

### Embeddings
- Embeddings: Vecteurs de données associés à chaque token ID qui contient la représentation numérique du sens d'un mot (des milliers de données pour chaque token) (Distance entre les mots)
- Les embeddings permettent au modèle de trouver les mots les plus proches selon les relations entre les mots dans les données d'entrainement.

## Résumé
- Mots > Tokens > Token-ID > Embeddings > Encodage positionnel (sens de la position des mots) > Self-Attention ou multi-head attention (sens dans le contexte)

## Ressources
- [Hugging Face](https://huggingface.co): Librairie de modèles AI
- [GPT Tokenizer Playground](https://gpt-tokenizer.dev)
- Exemple d'embedding: Word2Vec
