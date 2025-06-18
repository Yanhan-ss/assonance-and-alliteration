# assonance-and-alliteration
The repository shows three methods of training a language model to generate poems with semantic and phonetic constraints.
Mainly, we want to have a model that can generate fixed-length, four-line poems. Each poem contains two pairs of rhymes, a high level of assonance(repetition of certain vowels within a line), and a high level of alliteration (repetition of initial phonemes within a line). 

First method: hand-crafted generation rule.
The generator is built based on an existing character-level poetry generation model [ByGPT5](https://github.com/potamides/uniformers). The original model can rhyme and follow meter constraints very well, but it does not have a good level of alliteration. 
By boosting the probabilities of selecting certain words, we built a new generator that successfully outputs poems that contain rhymes, a high level of assonance, and a high level of alliteration. 

Second method: fine-tune the model on a large poetry dataset.
The fine-tune GPT-2 file exhibits the code for fine-tuning a GPT-2 model on a large poetry dataset. The fine-tuned model is capable of generating fixed-length, four-line poems, but it does not adhere to phonetic constraints as well as the character-level model above. 

Third method: PPO training.
The Proximal Policy Optimization (PPO) training is intended to motivate the GPT-2 model to increase its score for alliteration and assonance. We reward the model when the score is high and penalize it when the score is low. But the result is not so ideal. 

Conclusion: ByGPT5 with the hand-crafted generation rules (first method) is the best for generating poems that follow both semantic and phonetic constraints. 
