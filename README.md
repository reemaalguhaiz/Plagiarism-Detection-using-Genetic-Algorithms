
This project presents an intelligent Plagiarism Detection System built using Python, leveraging Genetic Algorithms (GA)
a metaheuristic optimization technique inspired by natural selection. Instead of relying solely on traditional string-matching algorithms, the system models the text similarity and plagiarism detection task as an optimization problem, searching for the most optimal subset of shared features and terms between an original document and a suspected document.

Key Components and Workflow

1. Text Preprocessing:
-Converts all raw text to lowercase, removes special characters, punctuation, and digits using regular expressions.
-Filters out common English stop words using the nltk library to focus on meaningful keywords.
-Applies the Porter Stemmer algorithm to reduce words to their root forms, ensuring variations of the same word are correctly matched.

2. Population Initialization:
-Combines the unique words of both texts to establish a comprehensive vocabulary space.
-Generates an initial population of binary chromosome vectors (where 1 represents the inclusion of a specific word feature and 0 represents its exclusion) using random initialization.

3. Fitness Evaluation (Fitness Function):
-Evaluates each individual chromosome by calculating the proportion of shared unique words between the texts relative to the total unique vocabulary.
-Returns a normalized fitness score ranging from 0.0 to 1.0, quantifying the degree of text overlap and potential plagiarism.

4. Genetic Operators:
-Selection: Ranks the population based on fitness scores and selects the top-performing parent solutions for reproduction.
-Crossover: Combines genetic material from parents at a random split point to produce stronger offspring solutions.
-Mutation: Introduces slight random variations into the offspring vectors based on a defined mutation rate to maintain genetic diversity and escape local optima.

5. Main Execution and Reporting:
-Iterates through multiple generations to progressively optimize the solutions.
-Outputs the best-performing individual vector, calculates the final similarity percentage, and classifies the text status into categories such as High Risk of Plagiarism, Moderate Similarity, or Low Similarity / Original Text.
 
Technology Stack
-Programming Language: Python 3
-Libraries: NLTK (Natural Language Toolkit), Regular Expressions (re), Random Module
-Environment: Google Colab 
