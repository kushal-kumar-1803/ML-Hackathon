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

Running

Place data/corpus.txt and data/test.txt (one word per line) in the data/ folder.
Then run:python hangman_final.py

This will:

Train the RL agent on corpus.txt

Periodically evaluate on test.txt

Run final evaluation with safe thresholding (0.05)

Print official final score (using the PDF formula)

Save training curves as training_curves_final_safe_eval.png

Official scoring

Final score uses the Hackathon formula exactly:Final Score = (SuccessRate * 2000) - (WrongGuesses * 5) - (RepeatedGuesses * 2)

Tuning

Adjust threshold in safe_action_selection() within hangman_final.py to shift the final score within a target band without retraining.

To reduce runtime for quick tests, lower N_TRAINING_EPISODES near top of the script.

License

MIT
