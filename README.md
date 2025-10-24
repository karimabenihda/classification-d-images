**Classification d’Images avec un Réseau Neuronal**

***Construire et entrainer un réseau neuronal dense minimaliste (DNN) sur une dataset (images 28×28, 10 classes) .Pour chargement et normalisation des images, construction d’un modèle Keras simple, entrainement et évaluation.*** 

**Lien trello:https://trello.com/b/ReHmBE1Q/classification-dimages**

**🧩 Étape 1 :Importation des modèles et chargement du dataset**
***Charger Fashion MNIST via Tensorflow.keras.datasets.***

***télécharger data et tester les shapes du train & test***

***afficher les articles avec matplotlib***

***Visualiser la Répartition des classes dans le dataset d'entraînement pour savoire si le dataset est equilibrer ou non car si on a la dominance d'une classes sur les autre classes le model va focucer sur celle qui est dominante***

***différence entre train loss et val loss:***
    ***Train loss → il mesure à quel point ton modèle se trompe sur les images qu’il connaît déjà.***
    ***Val loss → il mesure à quel point il se trompe sur de nouvelles images qu’il n’a jamais vues.***

***🧠 Création du modèle (Sequential):***
***Tu construis un réseau de neurones simple (DNN) avec Keras.Ce modèle contient 3 couches :***

***1.Flatten(input_shape=(28, 28))***
***->Transforme l’image 2D (28x28 pixels) en un vecteur 1D (784 valeurs).***
***->C’est comme “dérouler” l’image pour pouvoir l’envoyer dans le réseau.***

***2.Dense(128, activation='relu')***
***->Couche entièrement connectée (128 neurones).***
***->Fonction d’activation ReLU : garde les valeurs positives, met les négatives à 0 → aide à apprendre les motifs non linéaires.***

***3.Dense(10, activation='softmax')***
***->Couche de sortie avec 10 neurones (parce qu’il y a 10 classes à prédire, par exemple les chiffres de 0 à 9).***
***->Softmax transforme les sorties en probabilités (la somme = 1).***

***⚙️ Compilation du modèle***

***Tu définis comment le modèle va apprendre :***

***optimizer='adam' → Algorithme d’optimisation rapide et efficace.***

***loss='sparse_categorical_crossentropy' → Fonction de perte adaptée à une classification multi-classes avec labels entiers (0–9).***

***metrics=['accuracy'] → Pour suivre la précision pendant l’entraînement.***

***🧠 EarlyStopping:***
***Tu utilises EarlyStopping pour arrêter automatiquement l’entraînement quand le modèle ne s’améliore plus.***

***🧠 Entraînement du modèle: ***
***->X_train, y_train: Données d’entraînement.***
***epochs=20: Nombre maximal de cycles d’apprentissage.***
***->validation_data=(X_test, y_test): Données utilisées pour évaluer la performance du modèle à chaque époque.***
***->callbacks=[early_stop]: Utilise le mécanisme EarlyStopping pour arrêter l’entraînement si la performance cesse de s’améliorer.***


***🧠 Visualisation des performances du modèle:***
***-> 1er subplot(Train accuracy vs Validation accuracy):	Montrer comment la précision du modèle évolue à chaque époque.***

***-> 2e subplot(Train loss vs Validation loss):	Montrer comment la perte diminue (ou augmente) pendant l’apprentissage.***

**🧩 Étape 2 : Rédiger le rapport (README.md)**



