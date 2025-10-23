<p align="center">
  <img src="https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExZ2dnZWZoYzY0Nmh3Y3ptNXdhamdqcW9qMjIzb28zZ3VxOXB3Z3BkeCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/Lq9x8oIjtTbRcA5lm9/giphy.gif" width="140" alt="Tennis and ML animation" />
  <h1 align="center">🎾 NetGain: A Tennis Point Prediction Tool</h1>
  <p align="center"><b>University of Tennessee FDAC — Fall 2025</b></p>
</p>

---

## 📘 Overview

**NetGain** is a data-driven tennis analytics project that uses machine learning to model and predict shot patterns in professional tennis matches. The goal is to turn large quantities of point-level shot data into meaningful insights that can help players, coaches, and fans understand — and even anticipate — what happens next on the court.

---

## 🎯 Objectives

1. **Exploratory Data Analysis (EDA)**  
   Begin by aggregating and visualizing tennis shot data to identify basic patterns such as:
   - Rally length distributions 
   - Common serve locations  
   - Frequency and distribution of shot types  
   - Heatmaps of shot placement and outcomes  

3. **Machine Learning Models**  
   Develop models that predict which player wins the point or what the next shot will/should be.  
   - **Baseline:** Simple Logistic Regression Model 
   - **Advanced:** RNN or LSTM to model temporal dependencies within rallies  

4. **(Stretch Goals) Reinforcement Learning & App Development**  
   - Design a **reinforcement learning (RL)** agent capable of recommending optimal/probable shot choices based on game state  
   - Optionally, build a **web app** or interactive dashboard to explore predictions and visualizations dynamically  

   *If these stretch goals are not reached, results will instead be presented in a detailed written paper with visual summaries (tables and plots) and discussion.*

---

## 💡 Motivation

While tennis players are often encouraged to “forget the last point,” meaningful trends emerge over time — serving tendencies, shot preferences, and response strategies. By capturing these patterns, we aim to quantify the “memory” of a match and leverage it for prediction.

The structured nature of tennis data (two players, discrete shots, and fixed court geometry) makes it an ideal testbed for sequential machine learning.  

Additionally, with U.S. tennis participation recently rising to **25.7 million players** ([USTA, 2025](https://www.usta.com/en/home/stay-current/national/u-s-tennis-participation-surges-to-new-high-of-25-million-players.html)), there is growing interest in analytical tools that make the sport more understandable and data-driven.

---

## 📊 Dataset

**Source:** [SCORE Sports Data Repository](https://data.scorenetwork.org/tennis/tennis-shot-level-data.html)  
**Base Dataset:** *Grand Slam Tennis Shot-Level Data* (derived from Jeff Sackmann’s Match Charting Project)

Each row corresponds to a **single tennis shot**, described by features like:
- `ShotHand`, `ShotType`, `ShotDirection`, `ShotDepth`  
- `ServeDirection`, `OutcomeType`, `ErrorType`  
- Contextual info such as `Tournament`, `Round`, and `WinningPlayer`

**Data Summary:**

| League | Tournament | Shots Recorded |
|:--------|:------------|:----------------:|
| ATP | Australian Open | 635,064 |
| ATP | Roland Garros | 480,872 |
| ATP | US Open | 587,466 |
| ATP | Wimbledon | 457,591 |
| WTA | Australian Open | 291,544 |
| WTA | Roland Garros | 201,414 |
| WTA | US Open | 237,832 |
| WTA | Wimbledon | 190,204 |

These datasets allow us to explore both short-term (within a point) and long-term (match-wide) strategy patterns.

We will likely constrain our project to one or two of the eight datasets, as they are fairly large.

We believe the **Roland Garros** tournament is a good starting point, as rallies tend to last longer on clay, making for longer/richer episodes for our temporal models.

---

## ⚙️ Running the Project

```bash
# Clone the repo
git clone https://github.com/fdac25/tennis.git
cd tennis

# (Optional) Create and activate a virtual environment
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows

# Install dependencies
pip install -r requirements.txt

# Launch an example notebook
jupyter notebook notebooks/01_eda.ipynb
```

## 📈 Expected Outcome

- ✅ **Deliverable:** Machine learning model(s) that can predict the next shot or the winner of the point 
- 🧩 **Insights:** Visualizations and analysis showing player tendencies and model accuracy  
- 🌟 **Stretch Goals:**  
  - Reinforcement learning agent for shot recommendation  
  - Interactive app for dynamic visualization and exploration  

---

### 🙏 Acknowledgments

This project made use of OpenAI's ChatGPT (GPT-5, October 2025) to assist with:
- Drafting and formatting this README  
- Refining project documentation  
- Providing feedback and guidance on Python code structure and data visualization  

All content and code were reviewed, edited, and validated by the project authors.

---

## 📚 References

1. OpenAI, “ChatGPT (Oct 2025 version),” San Francisco, CA: OpenAI.  
2. USTA, [“U.S. Tennis Participation Surges to 25.7 Million Players,”](https://www.usta.com/en/home/stay-current/midatlantic/u-s--tennis-participation-surges-to-new-high-of-25-7-million-pla.html) Feb 19 2025.  
3. [SCORE Sports Data Repository](https://data.scorenetwork.org/tennis/tennis-shot-level-data.html)  
4. [Jeff Sackmann’s Match Charting Project](https://www.tennisabstract.com/charting/meta.html)

---

<p align="center"><i>“Tennis is 90% mental — the other half is data.”</i> 🎾</p>

