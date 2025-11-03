# 🧠 Self-Driving Car using Q-Learning  

## 📌 Overview  
This project demonstrates a simple **Reinforcement Learning (Q-Learning)** approach for teaching a car agent to navigate a grid environment safely, avoid obstacles, and reach its destination optimally.  

The project includes:  
- A **custom environment** simulating a small driving grid.  
- A **Q-Learning agent** that learns through trial and error.  
- **Training**, **testing**, and **performance analysis** modules.  
- A **documentation report** included for submission.  

---

## 🗂️ Project Structure  

self_driving_qlearning/
│
├── drivingenv.py # Environment (grid, obstacles, reward logic)
├── agent.py # Q-learning algorithm and agent behavior
├── train_agent.py # Training and reward plotting
├── test_agent.py # Testing trained agent accuracy
├── performance_analysis.py # Reward trends and performance visualization
├── training_rewards.pkl # Saved rewards from training
├── report.docx / report.pdf # Final documentation report
└── README.md # This file


---

## 🚗 How It Works  

1. **Environment Setup (`driving_env.py`)**  
   - The car starts at `(0,0)` on a `5x5` grid.  
   - The goal is `(4,4)` and obstacles are placed in between.  
   - The agent receives:  
     - `+10` → reaching goal  
     - `-10` → hitting obstacle  
     - `-1` → normal move  

2. **Agent (`q_learning_agent.py`)**  
   - Learns using **Q-Learning** with epsilon-greedy policy.  
   - Updates Q-values based on exploration and reward feedback.  

3. **Training (`train_agent.py`)**  
   - Trains for 1000 episodes.  
   - Tracks rewards and saves progress to `training_rewards.pkl`.  
   - Plots the **learning curve**.  

4. **Testing (`test_agent.py`)**  
   - Runs the trained model for multiple test episodes.  
   - Calculates success rate (accuracy).  
   - Displays reward distribution.  

5. **Performance Analysis (`performance_analysis.py`)**  
   - Loads reward data.  
   - Computes mean, max, min, and standard deviation.  
   - Plots moving-average learning trend.  

---

## ⚙️ Installation & Execution  

1️⃣ Install dependencies  
```bash
pip install numpy matplotlib
2️⃣ Train the agent
python train_agent.py
3️⃣ Test the trained model
python test_agent.py
4️⃣ Analyze performance
python performance_analysis.py

 📈 Performance Analysis
     he trained agent is evaluated using two key metrics:
     
     1️⃣ Trend Analysis
     hows how the **total reward** evolves over episodes, indicating the agent’s learning      rogress.
     
     2️⃣ Accuracy Evaluation
     alculates the **success rate** of the trained agent in reaching the goal.
     
     oth results are visualized through reward and accuracy plots.
     
---

🧾 Documentation Report
A detailed report (report.docx / report.pdf) is included.
It covers:
Problem statement
Objective
Methodology (Q-Learning explanation)
Implementation snapshots
Results and graphs
Conclusion



🧠 Key Learnings

How Q-Learning helps an agent make decisions based on rewards.
Exploration vs. exploitation balance.
Using reward trends to measure learning progress.
Visualization of reinforcement learning behavior.



🧩 Future Enhancements
Add dynamic traffic or multiple moving obstacles.
Extend to continuous environments using Deep Q-Networks (DQN).
Integrate OpenAI Gym interface for benchmarking.



👩‍💻 Author
Mekha Sindhu

