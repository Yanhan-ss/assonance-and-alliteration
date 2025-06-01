# assonance-and-alliteration
The generator is built based on the existing character-level model [ByGPT5](https://github.com/potamides/uniformers). The original model can rhyme and follow meter constraints very well, but it does not have a good level of alliteration. We created a new generator that aims to generate poetry that contains rhymes, a high level of assonance, and a high level of alliteration. 

Another file shows the code for fine-tuning a GPT-2 model on a large poetry dataset. The fine-tuned model is capable of generating fixed-length, four-line poems, but it does not adhere to phonetic constraints as well as the character-level model shown above. 
