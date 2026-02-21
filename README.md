# 🌱 Green AI: Intelligent LLM Routing & Energy Optimization

This project introduces a Smart Orchestration Layer designed to optimize the carbon footprint and operational costs of Generative AI. By analyzing prompt complexity in real-time, the router dynamically selects the most energy-efficient model (Small, Medium, or Large) without compromising output quality.


### 🎯 The Problem: The Environmental Cost of AI

Inference for Large Language Models (LLMs) requires significant computational power. Using a 175B+ parameter model for simple tasks like text formatting or basic Q&A is both financially expensive and ecologically unsustainable.


### 🚀 Key Features

- **Prompt Complexity Profiling**: Real-time analysis of user inputs to determine the required reasoning level.
- **Energy Benchmarking**: Implementation of an energy consumption model based on GPU TDP (Thermal Design Power), inference latency, and token count.
- **Carbon Baseline Comparison**: A built-in evaluation tool comparing the Router's performance against a standard "Static Baseline" (always using the largest model).
- **Multi-Model Strategy**: Routes tasks between Small Language Models (SLMs) like Phi-3 and Large models like Llama-3 or GPT-4.


### 📊 Impact & Results

Through intelligent routing, this system achieves:
- **~40% Reduction in $CO_2$ Emissions** (based on test dataset benchmarks).
- **Lower Inference Latency** for simple tasks by utilizing optimized small models.
- **Significant Cost Savings** by reducing unnecessary high-token-cost API calls.


### 🛠️ Tech Stack

- **Language**: Python
- **Machine Learning**: Scikit-Learn (for the routing logic)
- **Data Analysis**: Pandas, NumPyVisualization: Matplotlib, Seaborn
- **Metrics**: Custom Energy Estimator (mWh/token)


### 📖 Methodology

The core logic relies on a **Complexity Score** calculated from prompt features. This score is matched against the **Energy Efficiency Ratio** of available models:

1. **Low Complexity** -> Routed to **Small Models** (High Energy Savings).

2. **Medium Complexity** -> Routed to **Balanced Models**.

3. **High Complexity** -> Routed to **Large Models** (Maximum Reasoning).


### 🚀 How to Use

1. **Clone the repository** :
```bash
git clone https://github.com/LeJ-04/green-ai-prompt-routing.git
```

2. Install requirements:
```bash
pip install -r requirements.txt
```
