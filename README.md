# Tuition-log

# Day 1

# Git, GitHub, and Basic Version Control Concepts
# 📘 Part 1: Core Concepts
## Git
Git is an open-source Version Control System (VCS) that helps developers manage and track changes in source code during software development.

## GitHub
GitHub is a web-based platform that hosts Git repositories. It enables collaboration, code sharing, and version tracking, allowing developers to work together on projects.

Development Flow

Program ➝ Open Source ➝ Git (VCS)


### 💡 What is Computer Science?
Computer Science (CS) is an engineering field. Unlike subjects such as math that have single correct answers, CS involves finding **multiple possible solutions** to a problem. Often, the challenge is to **define the right question**, and then build the **most efficient solution** to solve it.

### ☁️ Microsoft OneDrive
Microsoft OneDrive is a **cloud-supported storage system**. It is managed by **data centers** that consist of multiple **servers** providing users access to files anywhere, anytime.

---

## Part 2: Learning GitHub & Commands

### ⚠️ Terminal Commands

| Command     | Description                   |
|-------------|-------------------------------|
| `cd`        | Change directory               |
| `mkdir`     | Create a new directory         |

### 🔁 Git & GitHub Commands

| Command                    | Description                                           |
|----------------------------|-------------------------------------------------------|
| `git clone <url>`          | Clone a repository from GitHub to your local machine |
| `git add .`                | Add all new or changed files to staging              |
| `git commit -m "message"`  | Commit staged changes with a message                 |
| `git push`                 | Push your local commits to the GitHub repository     |

### 📚 Key GitHub Terms

- **Repository (repo):** A space to store your code, documentation (like this README), and other files.
- **Upstream:** A GitHub repo that is not the original one you cloned or forked.
- **Fork:** A personal copy of a repo that lets you freely experiment with changes.
- **Branch:** A version of the codebase used to develop features, fix bugs, or experiment without affecting the main code.

---

# Day 2

## AI, Machine Learning (ML), and Deep Learning (DL)

### 🔍 Definitions

- **AI (Artificial Intelligence):** Includes all technologies that mimic human learning, reasoning, and problem-solving.
- **ML (Machine Learning):** A subset of AI that uses data to learn patterns and make predictions.
- **DL (Deep Learning):** A further subset of ML that uses neural networks to learn automatically from large datasets.


### 🤖 Machine Learning vs Deep Learning

| 구분              | 머신러닝 (Machine Learning)                                         | 딥러닝 (Deep Learning)                                         |
|-------------------|---------------------------------------------------------------------|----------------------------------------------------------------|
| 정의              | 데이터를 기반으로 학습하는 AI 기법                                  | 신경망(Neural Network) 기반의 학습                             |
| 특징              | 데이터에서 패턴을 찾아 예측                                          | 다층 신경망을 사용하여 자동으로 특징 추출                      |
| 데이터 의존성     | ↓ 낮음                                                               | ↑ 높음                                                         |
| 학습 속도         | 빠름                                                                 | 느림                                                           |
| 모델 예시         | SVM, 랜덤 포레스트, KNN, 선형 회귀, 로지스틱 회귀 등                | CNN, RNN, LSTM, GAN, Transformer 등                            |
| 응용 분야         | 추천 시스템, 질병 예측, 금융 모델링                                 | 이미지 인식, 음성 인식, 자율주행, 번역, 생성 AI               |

---

## Supervised vs Unsupervised Learning

| 구분              | 지도학습 (Supervised Learning)                                      | 비지도학습 (Unsupervised Learning)                             |
|-------------------|---------------------------------------------------------------------|----------------------------------------------------------------|
| 정의              | 정답(라벨)이 있는 데이터를 학습                                     | 정답(라벨) 없이 데이터를 학습                                  |
| 목적              | 입력 데이터를 보고 정답을 예측                                      | 데이터의 숨겨진 패턴을 찾음                                    |
| 입력 데이터       | (입력값, 정답) 쌍이 존재                                            | 입력값만 존재 (정답 없음)                                     |
| 출력 값           | 특정 라벨(분류) 또는 수치 값(회귀) 예측                            | 그룹(클러스터) 할당 또는 패턴 발견                            |
| 대표 모델         | KNN, SVM, 결정 트리, 랜덤 포레스트, 선형 회귀, 로지스틱 회귀, 신경망 등 | K-Means, DBSCAN, PCA, 군집 분석, 연관 규칙 분석 등             |
| 예시              | 스팸 메일 분류, 손글씨 숫자 인식, 가격 예측                         | 고객 세분화, 이상 탐지, 추천 시스템                            |

---

## Numpy
다차원 배열(Matrix)의 빠른 연산

## Pandas
데이터에 대한 표 형식의 표현

## Matplotlib
데이터 그래프 시각화 처리

---

# DAY 3

## Boxplot

```python
import matplotlib.pyplot as plt
import numpy as np

np.random.seed(10)
data = np.random.randn(50) * 10  # 평균 0, 표준편차 10을 따르는 정규분포 데이터
data = np.append(data, [50, -40])  # 이상치 추가

# 박스플롯 그리기 (이상치 표시)
plt.boxplot(data)

# 제목 및 라벨 추가
plt.title("Box Plot with Outliers")
plt.ylabel("Value")
plt.show()
```
## How to translate a boxplot

# 📦 Boxplot Interpretation

| Term | Description |
|:-----|:------------|
| **Minimum** | Position 1.5 IQR below the first quartile (Q1) |
| **First Quartile (Q1)** | Marks the 25% position at the bottom of the box |
| **Second Quartile (Q2)** | Median represented by the line inside the box, indicating 50% position |
| **Third Quartile (Q3)** | Marks the 75% position at the top of the box |
| **Maximum** | Position 1.5 IQR above the third quartile (Q3) |
| **Interquartile Range (IQR)** | The range between Q1 and Q3 |
| **Whisker** | Extends from the box to indicate the range of the data, up to the smallest and largest values within 1.5 IQR |
| **Outlier** | Data points beyond the minimum and maximum; if any exist, they are plotted beyond the whiskers |

![image](https://github.com/user-attachments/assets/cb717364-0953-4395-a32e-e450d6ac82f8)

## Iris Data set
🌸 Iris Dataset and KNN Algorithm
📘 Part 1: Iris Dataset
🌼 What is the Iris Dataset?
The Iris dataset is a famous dataset introduced by statistician Ronald Fisher in 1936.
It is commonly used for testing machine learning models and data analysis.

Sepal Length (cm) | Sepal Width (cm) | Petal Length (cm) | Petal Width (cm) | Species
5.1 | 3.5 | 1.4 | 0.2 | setosa
4.9 | 3.0 | 1.4 | 0.2 | setosa
4.7 | 3.2 | 1.3 | 0.2 | setosa
4.6 | 3.1 | 1.5 | 0.2 | setosa
5.0 | 3.6 | 1.4 | 0.2 | set

# 📘 Part 2: K-Nearest Neighbors (KNN)
# 🤔 What is KNN?
K-Nearest Neighbors (KNN) is a simple and widely used machine learning algorithm.
It classifies new data points based on the labels of the K closest data points.

# 💡 How KNN Works:
When a new data point is given, find the K nearest data points in the existing dataset.

Determine the most common class (species) among those K points.

Assign the new data point to that class.

# ℹ️ Tip:

A small K (e.g., K=1) means the prediction is highly influenced by nearby points.
A larger K (e.g., K=10) smooths the decision boundary and follows broader trends.

# Formulas

## Standardization Formula: 

Z = (X - μ) / σ

X : Original data
μ : Mean
σ : Standard Deviation

Distance Calculation (Euclidean Distance)

For data generalized to N dimensions, the distance between two points P1(x₁, x₂, ..., xₙ) and P2(y₁, y₂, ..., yₙ):

In 2 dimensions:

d(P₁, P₂) = √((x₁ - x₂)² + (y₁ - y₂)²)

In N dimensions:

d(P₁, P₂) = √(∑ (i=1 to n) (xᵢ - yᵢ)²)

