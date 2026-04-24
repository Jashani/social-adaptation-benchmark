# Social adaptation benchmark

A benchmark for social adaptation in LLMs. The benchmark evaluates whether LLMs can (and do) adapt their behaviour towards a partner based on implicit behavioral evidence.

## How it works

- The LLM (Helper) gives clues to a partner (Selector) to identify a target word among six similar options.
- The Helper is told their partner is a "beginner English learner," an "8-year-old child," or a "native speaker". The Selector is always instructed the same way, without mentioning personas.
- The game runs for 25 rounds per condition. The Helper sees the partner's choices and reasoning, allowing for style adjustment.
- This happens twice: once in a controlled task where the answers are hinted to the Selector, and once in a "natural" task where there are occasional forced errors and no hints.
- The primary score is a Cohen's d for the convergence of explanation style from "accommodating" to "adapted". This measures if the "accommodation gap" (the difference in how the model treats a "learner" vs. a "native") closes as the partner demonstrates competence.

## Links

Originally implemented on [Kaggle](https://www.kaggle.com/code/hiimyasha/social-adaptation-benchmark?scriptVersionId=307923746) for [DeepMind AGI Hackathon](https://www.kaggle.com/competitions/kaggle-measuring-agi/overview).

See [full writeup](https://www.kaggle.com/competitions/kaggle-measuring-agi/writeups/dynamic-partner-adaptation-benchmark).
