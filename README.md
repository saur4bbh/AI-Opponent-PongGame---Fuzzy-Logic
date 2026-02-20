🏓 Pong Game AI Opponent using Fuzzy Logic (Mamdani & TSK)

📌 Overview

This project implements an intelligent AI opponent for the classic Pong game using Fuzzy Logic Control Systems.

The AI paddle movement is controlled using two different fuzzy inference approaches:

Mamdani Fuzzy Inference System
Takagi–Sugeno–Kang (TSK) Fuzzy Model

The objective of this project is to demonstrate how fuzzy logic can be applied to real-time decision-making in dynamic game environments and simulate human-like reasoning under uncertainty.

🧠 Fuzzy Logic Approach

1️⃣ Mamdani Model

Uses linguistic variables such as Near, Far, Fast, and Slow.

It is based on IF–THEN fuzzy rules.

The system applies:
Fuzzification
Rule evaluation
Aggregation
Defuzzification

It produces smooth and interpretable paddle movement.

Example Rule

IF Ball_Distance is Near AND Ball_Speed is Fast
THEN Paddle_Move is Up

2️⃣ Takagi–Sugeno–Kang (TSK) Model

This model uses fuzzy inputs but mathematical functions as outputs.

The outputs are weighted linear functions.

It is computationally faster than Mamdani and more suitable for real-time systems.

Example Rule

IF Ball_Distance is Near AND Ball_Speed is Fast
THEN Paddle_Move = a*(Distance) + b*(Speed) + c

🕹 Gameplay Logic

The game continuously tracks ball position and velocity every frame.
Ball and paddle positions are fed into the fuzzy controller.
Fuzzy inference is performed (Mamdani or TSK).
A crisp output is generated representing AI paddle direction and speed.
The paddle moves accordingly.

🚀 How to Run

Clone the repository

git clone https://github.com/saur4bbh/AI-Opponent-PongGame---Fuzzy-Logic

Navigate into the directory

cd AI-Opponent-PongGame---Fuzzy-Logic

Install dependencies

pip install -r requirements.txt

Run the game

python main.py

🔮 Future Improvements

Adaptive rule tuning

Neuro-fuzzy (ANFIS) integration

Performance benchmarking metrics

Difficulty scaling mechanism
