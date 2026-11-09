# DLP — Deep Learning Practice (DA5013)

Interactive study material for the NLP half of the IIT Madras BS course **Deep Learning Practice**, weeks 1–4.

**→ [Open the site](https://michaeldatascience.github.io/DLP/)**

Each page explains a mechanism, works through the real past-paper questions on it, then quizzes you. Definitions are hidden by default where it helps, so pages double as recall practice rather than just reference.

## Contents

| Page | Covers | What's interactive |
|---|---|---|
| [The DLP Spine](https://michaeldatascience.github.io/DLP/spine.html) | Weeks 1–4 overview | Glossary with click-to-reveal definitions, searchable |
| [Transformer Anatomy](https://michaeldatascience.github.io/DLP/anatomy.html) | Week 3 — parameter counting | Live counter; set V, d, L, ctx and watch the model assemble |
| [Tokenizer Lab](https://michaeldatascience.github.io/DLP/tokenizers.html) | Week 2 — BPE, WordPiece, Unigram | Step through merges on an editable corpus; Viterbi lattice |
| [The Three Architectures](https://michaeldatascience.github.io/DLP/architectures.html) | Weeks 1 & 3 — encoder/decoder families | Clickable flowchart; attention-mask grid |
| [The Memory Ledger](https://michaeldatascience.github.io/DLP/memory.html) | Week 4 — training memory and PEFT | Memory calculator with togglable levers |
| [Quiz 1 Mock Papers](https://michaeldatascience.github.io/DLP/mocks.html) | Assessment | Two 50-mark papers, timer, auto-marking, full solutions |
| [`notebooks/01_tokenizers_from_scratch.ipynb`](notebooks/01_tokenizers_from_scratch.ipynb) | Week 2 implementation | BPE, WordPiece and Viterbi in pure stdlib Python |

## The notebook

No `pip install` required — `collections` and `math` only.

```bash
jupyter notebook notebooks/01_tokenizers_from_scratch.ipynb
```

33 cells. Every section ends with an `assert` against a figure printed on the lecture slides: the 22-symbol starting vocabulary, `(i,n)` winning at count 7, the WordPiece scores to three decimals, `whereby → where|by` at −15.55 with all four lattice intermediates, and `63/336/768` over 4096. Part 6 adds `transformer_params()` and `training_memory_gb()`, checked against all sixteen published past-paper answers.

A clean run means your implementation agrees with the course. Three exercises are left open.

## Two errors found in the course material

- The week-2 deck's final Viterbi lattice node reads **−15.51** for `whereby`. The correct sum is −8.21 + −7.34 = **−15.55**. Every intermediate value on the slide matches this computation, so it is a typo in the last node, not a different method.
- The deck's WordPiece score table lists only the pairs already shown for BPE, among which `(a,d)` at 0.167 wins. Over *every* pair in the corpus the real winner is `(r,y)` at 0.333, because `y` occurs once and `r` three times. Both illustrate the same rule — rare halves beat common halves at equal pair count.

## Technical notes

Every page is a single self-contained HTML file. No build step, no dependencies, no framework. The only external request is to Google Fonts. Both light and dark themes are supported and follow the system setting.

Pages were written as Claude artifacts and wrapped with a standard HTML skeleton for standalone hosting.

## Sources

Built from the week 1–4 lecture decks, both 2026 past Quiz-1 papers with their answer keys, and graded assignments 1–4. Numeric answers were computed and verified against the official accepted ranges.

Course material belongs to IIT Madras. Everything in this repository is independent study work.
