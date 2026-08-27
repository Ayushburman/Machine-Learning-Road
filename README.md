# Machine-Learning-Road

AI/ML // FIELD MANUAL

PRACTICAL DEPLOYMENT GUIDE
Master the AI/ML field from first principles to shipped systems.

This manual sequences AI/ML into six operational phases. Each phase has a concrete objective, skills to acquire, completion signals, and a checkpoint project.

Reading is not mastery. Deployed code is.

⸻



00 — FIELD OVERVIEW

Metric	Target
Total Phases	06
Realistic Timeline	9–14 months
Projects to Ship	12+
Daily Commitment	1.5–3 hours
Mode	Self-directed
Status	Active


⸻

01 — PHASE ROADMAP

Sequential — do not skip ahead.

⸻

PHASE 00 — FOUNDATIONS

Mathematical & Programming Bedrock

Objective:
Be able to read an ML paper’s notation and implement its core equation without a library.

Acquire

* Linear algebra:
    * Vectors
    * Matrix operations
    * Eigen-decomposition
    * SVD
* Calculus:
    * Gradients
    * Partial derivatives
    * Chain rule
* Probability:
    * Probability distributions
    * Bayes’ theorem
    * Expectation
    * Variance
* Python:
    * NumPy
    * Pandas
    * Vectorized operations
    * Avoid unnecessary loops

Signals You’re Done

* You can derive gradient descent from scratch on paper.
* You can implement matrix multiplication without numpy.dot.
* You read ∇L(θ) and know exactly what needs to be computed.

Checkpoint Project

Linear Regression From Scratch

Implement linear regression using only NumPy:

1. Normal equation
2. Gradient descent
3. Compare both solutions
4. Verify that they converge to approximately the same weights

Constraint: No scikit-learn.

⸻

PHASE 01 — CLASSICAL ML

Supervised & Unsupervised Learning

Objective:
Build intuition for when each classical algorithm wins, and understand why deep learning isn’t always the answer.

Acquire

* Regression
* Logistic regression
* Regularization:
    * L1
    * L2
* Decision trees
* Random forests
* Gradient boosting:
    * XGBoost
    * LightGBM
* SVMs
* k-NN
* Naive Bayes
* Clustering:
    * k-means
    * DBSCAN
* PCA
* Dimensionality reduction
* Bias-variance tradeoff
* Cross-validation
* Evaluation metrics

Signals You’re Done

* You choose an algorithm based on dataset characteristics, not hype.
* You can explain precision/recall tradeoffs to a non-technical person.
* You’ve deliberately diagnosed and fixed an overfit model.

Checkpoint Project

Kaggle Tabular Competition

Start with:

* Titanic
* House Prices

Build the complete pipeline:

EDA → Feature Engineering → Model Comparison → Evaluation → Leaderboard Submission

Include a written rationale explaining your decisions.

⸻

PHASE 02 — DEEP LEARNING

Neural Networks & Architectures

Objective:
Move from merely using PyTorch to understanding what backpropagation is doing under the hood.

Acquire

Neural Network Fundamentals

* Perceptrons
* MLPs
* Backpropagation
* Activation functions
* Loss functions

Optimization

* SGD
* Adam
* Loss landscapes
* Learning-rate schedules

Computer Vision

* CNNs
* Convolutions
* Pooling
* ResNet
* VGG

Sequential Models

* RNNs
* LSTMs
* Transformers
* Attention mechanism from scratch

PyTorch

* Autograd
* Custom datasets
* Training loops
* Model architectures

Signals You’re Done

* You’ve manually implemented backpropagation for a 2-layer neural network at least once.
* You can explain self-attention without looking at a diagram.
* You understand why transformers replaced RNNs for many sequence tasks.

Checkpoint Project

Build a Micro-Autograd Engine

Build a small automatic differentiation engine from scratch, inspired by projects such as micrograd.

Then:

* Train a CNN on CIFAR-10 using PyTorch.
* Target 85%+ test accuracy.
* Document the architecture, training process, and results.

⸻

PHASE 03 — SPECIALIZE

Pick ONE Track and Go Deep

Objective:
Depth beats breadth. Choose one specialization and build serious expertise.

Track Options

Computer Vision

* Object detection
* YOLO
* Image segmentation
* Diffusion models

NLP / LLMs

* Tokenization
* Embeddings
* Fine-tuning
* RAG
* Prompt engineering

Reinforcement Learning

* Markov Decision Processes
* Q-learning
* Policy gradients

Generative AI

* GANs
* VAEs
* Diffusion
* LLM agent frameworks

Signals You’re Done

* You can read a recent paper in your chosen track without relying on external explainers.
* You’ve fine-tuned or trained a nontrivial model rather than merely calling an API.
* You have an informed opinion about where your subfield is heading.

Checkpoint Project

Custom Computer Vision System

Fine-tune a pretrained object-detection model on a custom dataset that you collect yourself.

Document:

* Dataset creation
* Labeling
* Training
* Evaluation
* Failure cases
* What you would improve next

⸻

PHASE 04 — MLOPS

Deployment & Production Systems

Objective:
A model sitting in a notebook has limited real-world value. Learn to ship it.

Acquire

Model Serving

* FastAPI
* ONNX / TorchScript export
* Batching

Experiment Tracking

* Weights & Biases
* MLflow
* TensorBoard

Infrastructure

* Docker
* Basic CI/CD
* Data versioning
* Model versioning

Production ML

* Model monitoring
* Data drift
* Model degradation
* Retraining concepts

Cloud

Learn at least one:

* AWS SageMaker
* GCP Vertex AI
* Azure ML

Signals You’re Done

* A stranger can access your model through a REST endpoint.
* You’ve containerized and redeployed a model at least twice.
* You understand why model accuracy can silently degrade in production.

Checkpoint Project

Deploy an AI Model End-to-End

Take any Phase 02/03 model and:

1. Wrap it in a FastAPI service.
2. Containerize it with Docker.
3. Deploy it to a cloud instance.
4. Expose a REST API.
5. Build a simple frontend.
6. Send real inference requests to the deployed model.

⸻

PHASE 05 — PORTFOLIO

Proof-of-Work & Visibility

Objective:
Convert competence into a signal recruiters and research/IIT panels can understand within approximately 90 seconds.

Acquire

* 3–5 flagship GitHub repositories
    * Real READMEs
    * Original work
    * Clear documentation
* At least one end-to-end system
    * Live demo
    * Not just a description
* Written explainers:
    * Blog posts
    * YouTube
    * Technical documentation
* Contribution to at least one open-source ML repository

Signals You’re Done

* Someone unfamiliar with your work can understand your best repository in 2 minutes.
* You can defend every major design decision in your flagship project.
* Your GitHub looks like a body of work rather than a homework folder.

Checkpoint Project

Flagship AI System

Ship one polished, demoable, end-to-end AI system to GitHub.

Requirements:

* Production-quality README
* Architecture explanation
* Dataset documentation
* Model explanation
* Evaluation metrics
* Demo
* Deployment instructions
* Failure cases
* Future improvements

Make this your primary interview artifact.

⸻

02 — DEPENDENCY MAP

What Unlocks What

                         ┌─────────────────┐
                         │  MATH + PYTHON  │
                         └────────┬────────┘
                                  │
             ┌────────────────────┼────────────────────┐
             ▼                    ▼                    ▼
     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
     │ REGRESSION   │     │  CLUSTERING  │     │ METRICS /    │
     │ / TREES      │     │  / PCA       │     │ EVALUATION   │
     └──────┬───────┘     └──────┬───────┘     └──────┬───────┘
            └────────────────────┼─────────────────────┘
                                 ▼
                      ┌────────────────────┐
                      │ NEURAL NETWORKS    │
                      └─────────┬──────────┘
                                │
             ┌──────────────────┼──────────────────┐
             ▼                  ▼                  ▼
      ┌─────────────┐   ┌────────────────┐   ┌─────────────┐
      │ CNN → CV    │   │ TRANSFORMER    │   │ POLICY NETS │
      │             │   │ → NLP / LLM    │   │ → RL        │
      └──────┬──────┘   └───────┬────────┘   └──────┬──────┘
             └──────────────────┼────────────────────┘
                                ▼
                       ┌────────────────┐
                       │     SHIP IT    │
                       │     MLOps      │
                       └────────────────┘

Core Dependency Chain

Math + Python
      ↓
Classical ML
      ↓
Neural Networks
      ↓
Specialization
      ↓
MLOps
      ↓
Production System
      ↓
Portfolio / Proof-of-Work

⸻

03 — TOOL STACK

What to Actually Install

Category	Recommended Stack
Language / Core	Python 3.11+ · NumPy · Pandas · Matplotlib · Jupyter · VS Code
Classical ML	scikit-learn · XGBoost · LightGBM · statsmodels
Deep Learning	PyTorch · Hugging Face Transformers · TensorFlow
Experiment Tracking	Weights & Biases · MLflow · TensorBoard
Data	SQL · Kaggle datasets · Label Studio · CVAT
Deployment	FastAPI · Docker · AWS SageMaker · GCP Vertex AI
GPU Access	Google Colab · Kaggle Notebooks · Lambda / RunPod
Version Control	Git + GitHub · DVC · Conda / venv

⸻

Recommended Priority

If you’re overwhelmed by the number of tools, learn them in this order:

01. Python
02. NumPy
03. Pandas
04. Matplotlib
05. SQL
06. scikit-learn
07. Git + GitHub
08. PyTorch
09. Hugging Face
10. FastAPI
11. Docker
12. MLflow / W&B
13. Cloud

Rule: Don’t collect tools. Build systems with them.

⸻

04 — DAILY OPERATING RULES

Non-negotiables

01 — Code Every Day

* Code every single day, even if it’s only 30 minutes.

Why: Consistency compounds. Long gaps destroy momentum.

Frequency: DAILY

⸻

02 — Implement Before You Import

* Implement the algorithm from scratch before relying on a library.

Why: Build the mental model once, then use the production library afterward.

Frequency: PER TOPIC

⸻

03 — Ship Before Moving Phases

* Complete the checkpoint project before advancing to the next phase.

Why: Watching a course is passive completion. Shipping code demonstrates active competence.

Frequency: PER PHASE

⸻

04 — Read One Paper End-to-End

* Read at least one ML paper from beginning to end every week.

Start with foundational papers before moving toward current research.

Frequency: WEEKLY

⸻

05 — Push to GitHub

* Push meaningful work to GitHub with a real README.

Why: Public accountability turns your learning into visible proof-of-work.

Frequency: WEEKLY

⸻

06 — Explain What You Learned

* Explain what you learned to another person or write it down.

Use the Feynman Technique:

Learn
  ↓
Explain simply
  ↓
Find gaps
  ↓
Study gaps
  ↓
Explain again

Frequency: WEEKLY

⸻

05 — THE MASTER LOOP

The entire roadmap can be reduced to one operating loop:

                 ┌──────────────┐
                 │    LEARN     │
                 └──────┬───────┘
                        ↓
                 ┌──────────────┐
                 │  IMPLEMENT   │
                 └──────┬───────┘
                        ↓
                 ┌──────────────┐
                 │    BUILD     │
                 └──────┬───────┘
                        ↓
                 ┌──────────────┐
                 │    SHIP      │
                 └──────┬───────┘
                        ↓
                 ┌──────────────┐
                 │   EXPLAIN    │
                 └──────┬───────┘
                        ↓
                 ┌──────────────┐
                 │    REPEAT    │
                 └──────┬───────┘
                        │
                        └──────────────→

⸻

06 — FINAL RULE

DO NOT SKIP FOUNDATIONS
        ↓
DO NOT JUST WATCH COURSES
        ↓
IMPLEMENT THE CONCEPT
        ↓
BUILD A PROJECT
        ↓
SHIP IT
        ↓
DOCUMENT IT
        ↓
TEACH IT
        ↓
MOVE TO THE NEXT PHASE

END OF MANUAL

PROCEED TO PHASE 00.

TRUST THE SEQUENCE.
