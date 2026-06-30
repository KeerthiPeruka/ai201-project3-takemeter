# Project Planning

## Community Choice

This project uses cooking related Reddit communities because they contain many different types of cooking questions. Users ask for recipes, request help solving cooking problems, and participate in discussions about food. These communities provide a good variety of posts for a text classification task.

Communities used:

* r/Cooking
* r/AskCulinary
* r/Baking

---

# Classification Task

The goal is to classify each Reddit post into one of three categories based on its main purpose.

---

# Labels

## Recipes and Meal Ideas

Posts asking for recipes, meal ideas, ingredient ideas, or suggestions for what to cook.

Examples:

* What can I make with leftover chicken?
* Easy dinner ideas?

---

## Help and Troubleshooting

Posts asking how to solve cooking problems, ingredient substitutions, food safety questions, storage questions, or cooking techniques.

Examples:

* Why are my cookies flat?
* How do I de clump a sauce?

---

## Discussion and Opinions

Posts asking for recommendations, opinions, preferences, experiences, or general discussion.

Examples:

* What is the best cooking advice you have received?
* Cooking every day is a hassle.

---

# Hardest Edge Case

The most difficult examples involve ingredient substitutions and recipe modifications because they can appear to be both recipe requests and troubleshooting questions. During annotation, the main purpose of the post was used to decide the final label.

---

# Data Collection Plan

Collect at least 200 cooking related Reddit posts from multiple communities.

Each post will be manually reviewed and assigned exactly one label.

The dataset will then be divided into:

* Training
* Validation
* Test

---

# Evaluation Plan

The model will be evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix

These metrics provide both overall performance and performance for each individual label.

---

# Good Enough Performance

A fine tuned model accuracy of **50% or higher** on the test set will be considered acceptable because the dataset is relatively small and contains many short and ambiguous Reddit posts.

---

# AI Tool Plan

It helped explain errors, review sections of the training pipeline, and suggest changes to the hyperparameters. After testing different settings, I increased the number of training epochs from 3 to 5 and reduced the warmup steps from 50 to 10. I reran the notebook and verified that these changes improved the model accuracy from 23.3% to 50.0% before keeping them in the final project.