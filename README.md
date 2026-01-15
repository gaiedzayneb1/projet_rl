🧠 Résumé du projet : Reinforcement Learning from Human Feedback (RLHF) in Notebooks

Ce projet propose une implémentation pédagogique et pas à pas du framework RLHF (Reinforcement Learning from Human Feedback) à l’aide de Jupyter Notebooks. L’objectif est de montrer concrètement comment aligner un modèle de langage pré-entraîné (GPT-2) avec des préférences humaines en combinant apprentissage supervisé, apprentissage par renforcement et modèles de récompense.

🎯 Objectif principal

Adapter un modèle GPT-2 pré-entraîné afin qu’il génère uniquement des phrases à sentiment positif, en s’inspirant du principe du RLHF utilisé pour aligner des grands modèles de langage comme ChatGPT.

🔄 Principe du RLHF

Le RLHF est une méthode d’alignement des modèles de langage où le feedback humain n’est pas utilisé directement comme récompense, mais sert à entraîner un modèle de récompense. Ce modèle est ensuite utilisé dans une boucle de reinforcement learning.

Le processus se déroule en trois étapes clés :

Supervised Fine-Tuning (SFT)

Reward Model Training (RM)

Reinforcement Learning avec PPO

📊 Cas d’étude du projet

Au lieu de créer un chatbot avec des réponses classées par des humains, le projet simplifie le cadre RLHF en utilisant le dataset stanfordnlp/sst2, composé de phrases de critiques de films annotées comme positives ou négatives.

👉 Le rôle du feedback humain est ici simulé par les labels de sentiment.

📒 Contenu des notebooks
1️⃣ 1-SFT.ipynb – Supervised Fine-Tuning

GPT-2 est fine-tuné de manière supervisée sur le dataset SST-2.

Le modèle apprend à générer des phrases similaires aux critiques de films.

Le modèle obtenu est appelé SFT model.

2️⃣ 2-RM Training.ipynb – Reward Model

Un modèle de récompense est construit en ajoutant une reward head à GPT-2.

Ce modèle est entraîné pour prédire le sentiment (positif ou négatif) d’une phrase.

Il simule l’évaluation humaine de la qualité des générations.

3️⃣ 3-RLHF.ipynb – Reinforcement Learning avec PPO

Le modèle SFT est utilisé comme policy initiale.

Il génère des phrases qui sont évaluées par le reward model.

L’algorithme PPO (Proximal Policy Optimization) ajuste les paramètres du modèle pour maximiser la récompense (sentiment positif).

✅ Résultat final

Après l’entraînement RLHF :

GPT-2 est aligné pour produire majoritairement des phrases à sentiment positif.

Le projet démontre de façon concrète comment RLHF peut guider un LLM vers un comportement souhaité.


comprendre le fonctionnement interne de ChatGPT-like models

Excellent pont entre NLP, Deep Learning et Reinforcement Learning
