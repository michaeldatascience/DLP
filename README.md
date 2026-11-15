# DLP — Deep Learning Practice (DA5013) · Quiz 1 study set

Study material for weeks 1–4 of the IIT Madras BS course **Deep Learning Practice**: datasets, tokenization, transformers and GPT, fine-tuning and memory.

**→ [Open the site](https://michaeldatascience.github.io/DLP/)**

## Contents

| Page | Covers | What it is |
|---|---|---|
| [The Whole Cycle](https://michaeldatascience.github.io/DLP/cycle.html) | Weeks 1–4 | Raw text to a usable model in three parts, with shapes and numbers for a toy, GPT-1 or GPT-2 |
| [Quiz 1 Cheatsheet](https://michaeldatascience.github.io/DLP/cheatsheet.html) | Weeks 1–4 | The one notes page: every definition, formula and trap, a randomised formula drill, 52 rapid-fire questions |
| [Tokenizer Lab](https://michaeldatascience.github.io/DLP/tokenizers.html) | Week 2 | Step through BPE, WordPiece and Unigram on the lecture corpus |
| [Transformer Workshop](https://michaeldatascience.github.io/DLP/transformer.html) | Week 3 | Corpus to loss · one block with every number · parameter counter · three architectures and the causal mask |
| [Memory Workshop](https://michaeldatascience.github.io/DLP/memory.html) | Week 4 | The four copies · five memory techniques · LoRA on a real matrix · stacking them · exam questions |
| [Mock Papers](https://michaeldatascience.github.io/DLP/mocks.html) | Assessment | Two 50-mark papers with timer, auto-marking and solutions |
| [`notebooks/01_tokenizers_from_scratch.ipynb`](notebooks/01_tokenizers_from_scratch.ipynb) | Week 2 code | BPE, WordPiece and Viterbi in plain Python, asserted against the lecture slides |

Earlier single-topic pages (Spine, Transformer Anatomy, Three Architectures, Memory Ledger, One Block, From Corpus to Loss, Five Levers) are now tabs inside the two workshops.

## Two errors found in the course material

- The week-2 deck's last Viterbi node reads **−15.51** for `whereby`. The correct sum is −8.21 + −7.34 = **−15.55**.
- The deck's WordPiece score table lists only the pairs shown for BPE, among which `(a,d)` at 0.167 wins. Over every pair in the corpus the real winner is `(r,y)` at 0.333.

## Technical notes

Every page is one self-contained HTML file. No build step, no dependencies. The only external request is to Google Fonts; without internet the pages fall back to system fonts and still work. Light and dark themes follow the system setting. `.nojekyll` tells GitHub Pages to serve the files as they are.

## Sources

Built from the week 1–4 lecture decks, both 2026 past Quiz 1 papers with their answer keys, and graded assignments 1–4. Numeric answers were checked against the official accepted ranges.

Course material belongs to IIT Madras. Everything here is independent study work.
