# Transformer Training 01 — The Training Loop and the Objective

One loop, repeated: a batch of text, a forward pass, a loss, a backward pass, an update. What next-token cross-entropy measures, why its gradient is p − y, and what a real loss curve looks like, measured on a 5,376-parameter decoder that trains in a browser.

**Live site:** https://brendanjameslynskey.github.io/Transformer_Training_01_Training_Loop_and_Objective/

The loop (batch, forward, loss, backward, update); next-token cross-entropy and its gradient p−y; the default run's loss curve and plateau; training vs validation loss, perplexity; seeds and spread; how the trainer is checked.

## Live, animated companion

This deck is the slide companion to Part 2 (Training) of [Transformer Decoder Explained](https://transformer-decoder-explained.vercel.app/training), where the same model trains in your browser:

- [Chapter 1: The training loop](https://transformer-decoder-explained.vercel.app/training/01-training-loop)
- [Chapter 3: The objective](https://transformer-decoder-explained.vercel.app/training/03-objective)

## Where the numbers come from

Every measured number on these slides comes from the site's [results.md](https://github.com/BrendanJamesLynskey/transformer-explainer/blob/main/results.md) (seeded NumPy reference runs; CI recomputes them), filled in at build time from its `results.json`. Numbers from papers are cited on the slide with a link. The model is tiny (5,376 parameters, one book, a CPU): its runs show mechanisms, not what happens at scale, and the slides say so where it matters. GPU runs of the site's Colab notebooks are pending; no GPU number appears here.

Part of the [Transformer Training sub-hub](https://github.com/BrendanJamesLynskey/LLM_Hub_Transformer_Training) &middot; [LLMs hub](https://github.com/BrendanJamesLynskey/LLMs)
