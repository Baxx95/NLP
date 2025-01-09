# On parlera de NLP à GenAI

---

### **1. Naïve Bayes (modèle classique)**

#### **Explication simple :**
Imagine que tu as deux paniers :  
- **Panier A :** il contient 80 pommes et 20 bananes.  
- **Panier B :** il contient 30 pommes et 70 bananes.  

Si je te donne une pomme, tu as plus de chances de deviner qu'elle vient du Panier A, car il contient plus de pommes.

Naïve Bayes utilise cette logique pour deviner à quelle catégorie (classe) appartient un texte, en se basant sur les mots qu'il contient et leur fréquence dans chaque catégorie.

---

#### **Exemple concret :**
On veut classer des phrases comme "Spam" ou "Non-spam".  
- **Données d'entraînement :**
  - Spam : "Gagnez un iPhone maintenant", "Cliquez ici pour un cadeau".
  - Non-spam : "Bonjour, comment allez-vous ?", "Merci pour votre e-mail".

  Après analyse, on trouve :  
  - Le mot "Gagnez" apparaît 80% du temps dans les messages "Spam".  
  - Le mot "Merci" apparaît 90% du temps dans les messages "Non-spam".  

- **Phrase à analyser :** "Merci pour ce cadeau".  
  - Naïve Bayes calcule les probabilités pour chaque catégorie en se basant sur les mots.  
  - Si la probabilité est plus élevée pour "Spam", alors la phrase sera classée comme spam. Sinon, "Non-spam".

---

#### **Application pratique :**  
- **Classification des e-mails** : savoir si un e-mail est un spam ou non.  
- **Détection de sentiments** : déterminer si un avis est positif ou négatif.

---

### **2. Word2Vec (modèle avancé)**

#### **Explication simple :**
Imagine un jeu où tu dois mesurer les relations entre des mots. Si je te demande :  
- Quelle est la relation entre *"roi"* et *"reine"* ?  
- Tu réponds : *"homme"* et *"femme"* sont similaires à cette relation.  

Word2Vec apprend ces relations en transformant les mots en nombres (vecteurs) qui représentent leurs significations.

---

#### **Exemple concret :**  
- Phrase : "Le chien court dans le jardin."  
- Word2Vec transforme chaque mot en un vecteur (une liste de nombres) comme ceci :  
  - "chien" : [1.2, -0.3, 0.8, 0.5]  
  - "chat" : [1.1, -0.2, 0.7, 0.4]  

  On voit que les vecteurs de "chien" et "chat" sont proches, car ces mots ont des significations similaires.

---

#### **Application pratique :**  
- Trouver des synonymes : "chien" est proche de "chat", mais loin de "voiture".  
- Traduction automatique : comprendre que "chien" en français est proche de "dog" en anglais.

---

### **3. Transformers (modèle très avancé)**

#### **Explication simple :**
Imagine un super assistant qui peut lire tout un texte d'un coup et en comprendre le contexte.  
- Exemple : Si tu dis *"Le chat dort"*, un Transformer sait que "chat" est un animal. Mais si tu dis *"Le chat avec Jean s'est bien passé"*, il comprend que "chat" ici signifie "discussion".  

Les Transformers (comme GPT ou BERT) sont entraînés à lire des milliards de phrases pour deviner ce que tu veux dire, même si ce n’est pas explicite.

---

#### **Exemple concret :**  
**Tâche : Compléter une phrase.**  
- Input : "Le chat dort sur le..."  
- Le Transformer lit cette phrase et prédit des mots probables : "canapé", "lit", ou "tapis".  
- Il choisit "canapé" si c'est le mot le plus probable en fonction des données qu'il a apprises.

---

#### **Application pratique :**  
- **Génération de texte :** écrire des histoires ou des résumés.  
- **Traduction automatique :** convertir "Bonjour" en "Hello".  
- **Chatbots :** répondre intelligemment aux questions.

---

### Comparaison des modèles  
| **Critère**          | **Naïve Bayes**                          | **Word2Vec**                            | **Transformers**                     |
|-----------------------|------------------------------------------|------------------------------------------|---------------------------------------|
| **Simplicité**       | Facile à comprendre et rapide            | Plus complexe, nécessite plus de données| Très complexe, mais très performant  |
| **Données nécessaires**| Peu (fonctionne bien avec peu de données)| Moyen                                   | Beaucoup (énorme volume requis)      |
| **Applications**      | Spam, sentiment                         | Synonymes, relations                    | Résumés, traduction, génération de texte|

---




Le notebook sera un guide pratique pour tester quelques modèles (Naive Baise, WOrd2VEc, Gensim, Transformers) en Python avec des bibliothèques courantes comme scikit-learn, Gensim, et Transformers.
