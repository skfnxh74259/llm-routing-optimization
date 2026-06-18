# Cost-Aware LLM Routing Optimization

## Overview

Developed an optimization framework for routing prompts across large language models (LLMs) to maximize response quality while controlling inference costs. Formulated the routing problem as a Mixed Integer Linear Programming (MILP) optimization model using Pyomo and evaluated cost-performance tradeoffs across a benchmark dataset containing prompt-level results from dozens of LLMs.

The project explores how organizations can deploy a pool of models rather than relying on a single LLM, enabling higher performance at controlled operating costs through intelligent routing decisions.

## Tools & Technologies

* Python
* Pandas
* NumPy
* Pyomo
* HiGHS Solver
* Mixed Integer Linear Programming (MILP)
* Jupyter Notebook
* Matplotlib
* Git/GitHub

## Skills Demonstrated

* Operations Research
* Optimization Modeling
* Mathematical Programming
* Decision Analytics
* AI Model Evaluation
* Cost-Performance Analysis
* Constraint Optimization
* Data Analysis
* Data Visualization
* Experiment Design
* Model Selection
* Business Analytics

## Project Highlights

* Evaluated routing strategies across 30+ large language models
* Formulated prompt routing as a Mixed Integer Linear Programming (MILP) problem
* Designed budget, model pool size, and benchmark quality constraints
* Achieved 98.3% average performance while maintaining strict cost limits
* Identified diminishing returns from increasing model pool size beyond six models
* Quantified cost-performance tradeoffs for real-world AI deployment scenarios

## Objective

The goal of this project was to determine how prompts should be assigned across multiple LLMs in order to maximize response quality while minimizing inference costs. Rather than selecting a single model for every task, the framework dynamically chooses models subject to operational constraints such as budget limits, model pool size, and benchmark quality requirements.

## Dataset

**Source:** RouterBench Benchmark Dataset

The dataset contains prompt-level evaluation results across multiple language models.

Features included:

* Prompt ID
* Benchmark Dataset
* Model Name
* Binary Performance Score
* Inference Cost

The dataset consists of prompt-model pairs that capture the performance and cost of each model on a specific task.

## Methodology

### Data Preparation

* Loaded and validated prompt-model benchmark data
* Processed model performance scores and inference costs
* Constructed prompt weighting schemes for evaluation
* Created prompt-model cost and score matrices

### Optimization Model

Formulated the routing problem as a Mixed Integer Linear Program (MILP).

Decision variables included:

* Prompt-to-model assignment variables
* Model pool selection variables

Constraints included:

* Each prompt assigned to exactly one model
* Routing limited to selected models
* Maximum model pool size
* Budget limitations
* Minimum benchmark quality thresholds

Objective:

* Maximize weighted average performance score while satisfying operational constraints

### Baseline Policies

Compared optimized routing against:

* Single Best Model
* Single Best Model per Benchmark
* Oracle Routing Policy

### Experimental Analysis

#### Model Pool Size Analysis

Evaluated routing performance for model pools ranging from 1 to 10 models.

Key findings:

* Performance increased from 72.9% to 98.3%
* Significant gains were achieved by expanding the model pool from 1 to 6 models
* Returns diminished beyond approximately 6 models

#### Budget Sensitivity Analysis

Evaluated routing performance under multiple budget levels.

Key findings:

* Average performance improved from 94.2% to 98.3% as budget increased
* Performance gains plateaued beyond moderate spending levels
* Near-optimal performance was achievable without selecting the most expensive models

## Results

### Model Pool Experiment

* Performance increased from 72.9% with a single model to 98.3% with larger model pools
* A pool size of six models achieved near-optimal performance while maintaining cost efficiency

### Budget Experiment

* Average performance improved from 94.2% to 98.3% as budget constraints were relaxed
* Additional spending beyond moderate budget levels produced limited gains

### Overall Findings

* Intelligent routing significantly outperformed single-model deployment strategies
* Small collections of carefully selected models captured most available performance gains
* Optimization-based routing provided a practical framework for balancing AI quality and operating costs

## Key Takeaways

* Optimization techniques can substantially improve LLM deployment efficiency.
* Model diversity provides significant performance benefits compared to relying on a single model.
* Budget constraints have a measurable impact on achievable AI performance.
* Operations research and optimization methods can be effectively applied to modern AI infrastructure problems.
* Cost-aware routing frameworks offer a scalable approach for production AI systems.
