# Hangman Solver using Enhanced HMM + Reinforcement Learning

This project implements a Hangman solver using:

- Enhanced HMM-style oracle (pattern, position, trigram)
- Q-Learning reinforcement learning agent
- Safe evaluation filter to reduce low-confidence guesses (threshold = 0.05)
- Official Hackathon scoring formula

---

## Files

- `hangman_final.py` — main runnable script (training + evaluation + scoring)
- `data/corpus.txt` — training words (place your corpus here)
- `data/test.txt` — test words (place your test set here)
- `requirements.txt` — dependencies
- `.gitignore` — useful ignores

---

## Installation

```bash
git clone https://github.com/YOUR_USERNAME/hangman-rl-hmm.git
cd hangman-rl-hmm
python -m venv venv
source venv/bin/activate   # or venv\Scripts\activate on Windows
pip install -r requirements.txt
