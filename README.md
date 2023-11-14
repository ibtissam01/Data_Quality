# Data_Quality
Data Modeling TP 2 Preprocessing NLP 2023/2024
Pr. N. Daoudi 1/2 Data modeling
Preprocessing NLP
NB :
Tout au long de ce cette activité, nous allons travailler sur le contenu Texte et WORDS et mots
définis comme ce qui suit :
• Text= "Data virtualization is a concept and technology that allows organizations to
access and manage data from various sources in a unified and simplified manner,
without the need to physically move or replicate the data. It provides a layer of
abstraction that presents a virtual view of data from different sources, making it appear
as if it resides in a single, centralized location."
• WORDS= ["RUNNING", "Played", "AM", "BEAUtiful", "Dogs"]
• Mots= ["manges", "jouent", "suis", "suivons", "corpora","heureusement", "grandes",
"better"]
1. Avant de démarrer :
1.1 Assurer vous que la bibliothèque NLTK et bien installée et importée
import nltk
1.2 Télécharger en local les données nécessaires pour le traitement automatique du langage.
• nltk.download("wordnet") :utile pour lemmatisation
• nltk.download('stopwords') : utile pour supprimer les stopwords
• nltk.download('punkt') : utile pour tokenisation
• nltk.download('all'): telecharge en local le tout.
WordNet contient une structure hiérarchique de synonymes et de relations sémantiques entre les
mots. La lemmatisation, qui consiste à ramener les mots à leur forme de base (lemme), bénéficie
de l'accès à WordNet pour obtenir des informations lexicales et sémantiques plus riches.
Après la phase de collecte des données textuelles, l'exploration et le prétraitement du texte sont
des étapes cruciales dans le processus d'analyse en traitement automatique du langage naturel
(NLP). L'exploration révèle la nature profonde du corpus linguistique, identifiant les aspects clés
et les défis potentiels. Elle prépare ainsi le terrain pour le nettoyage des données, les
transformations nécessaires, et la normalisation du texte, rendant ainsi les données prêtes à être
utilisées par des modèles d'apprentissage automatique (objectif principale du cours textminig).
Ce TP couvre les différentes étapes de preprocessing du texte : la suppression des mots vides, la
et la ponctuation, la mise en minuscules, la lemmatisation, le stemming, et l'utilisation de
quelques techniques basiques de word embeddings (vectorisation).
Data Modeling TP 2 Preprocessing NLP 2023/2024
Pr. N. Daoudi 2/2 Data modeling
2. Normalisation
from nltk.corpus import stopwords
2.1 Suppression des mots vides
• Pourquoi les supprimer lors du prétraitement du texte?
• Supprimez les mots vides du texte.
2.2 Suppression de la Ponctuation
• Pourquoi la suppression de la ponctuation est-elle importante dans le prétraitement du texte?
• Supprimez la ponctuation du texte (penser à utiliser string.punctuation)
2.3 Transformation en Minuscules
• Quelle est l'importance de transformer le texte en minuscules ?
• Transformez WORDS en minuscules.
3. Tokenisation
• Qu’est-ce que la tokenisation ?
• from nltk.tokenize import sent_tokenize, word_tokenize
• Appliquer la tokenization sur le texte.
4. Lemmatisation & Stemming
4.1 Lemmatisation
• Qu'est-ce que la lemmatisation et en quoi diffère-t-elle du stemming?
• Utilisez WordNetLemmatizer pour lemmatiser la liste suivante
o words_tok = ["running", "played", "am", "beautiful", "dogs", “better”]
o pensez à utilizer part of speech!
• Appliquez WordNetLemmatizer() sur le texte.
• Et si on avait un contenu en français par exemple !
o mots = ["manges", "jouent", "suis", "suivons", "corpora","heureusement", "grandes",
"better"]
4.2 Stemming
• Pourquoi est-ce utilisé dans le prétraitement du texte?
• Appliquez le stemming au texte de différentes manières.
• Comparer les résultats.
• Quelle est la meilleure technique de stemming ?
5. Word Embeddings avec Word2Vec
• Qu'est-ce que Word Embeddings et pourquoi sont-ils utilisés dans le NLP?
• Appliquer le TfidfVectorizer et CountVectorizer sur le texte.
• Utilisez la bibliothèque Gensim pour créer des embeddings de mots (Word2Vec) à partir du
texte.
Etude de cas
Charger un contenu de votre choix à partir de nltk.corpus ou un autre répertoire de votre choix et
refaire l’ensemble des étapes du preprocessing.
NB : Travail en groupe de 3 personnes à rendre avant jeudi 16 novembre.
