# LLM Hallucinaton

## Executive Summary

## Problem

LLM is known to have hallucination problem since 2022. However, as models are getting better, the number of occurrences in hallucination reduces greatly. However, this does not mean that there will be no hallucination even in simple cases.  

Recently, I encounter a situation where LLM give me the wrong answer to a probability challenges. 

On a separate occasion, when asked "What is the limitation of LLM", Gemini returns a list which is extracted from blog post. This is not what I have expected as other LLM give me information extracted from papers.

### Hallucination in Probability Challenge

The following is part of the conversation on a probability challenge:

![alt text](<assets/Screenshot 2026-10-05 at 17.25.32.png>)

My answer is wrong and the following is the explanation from LLM

![alt text](<assets/Screenshot 2026-10-05 at 17.34.54.png>)

After a few rounds of explanation, it discover I was right

![alt text](<assets/Screenshot 2026-10-05 at 17.37.08.png>)

This is the first sign of hallucination.

When preparing for this exercise, I double check with another model (Claude):

![alt text](<assets/Screenshot 2026-10-05 at 17.42.48.png>)

I ask about earlier chat and the following explained that the other response was wrong:

![alt text](<assets/Screenshot 2026-10-05 at 17.44.58.png>)

I double check with ChatGPT with the original chat:

![alt text](<assets/Screenshot 2026-10-05 at 17.45.35.png>)
... more workings
![alt text](<assets/Screenshot 2026-10-05 at 18.07.17.png>)


[Source of ChatGPT](https://chatgpt.com/share/6ac34524-7e74-83ec-ab51-1d185d877cd1) 


### Reliable Source of Information
When asking a question, 


[Source of Gemini](https://share.gemini.google/xOjCs52VmWq7)


## Implications

With a mix of reliable and unreliable information in LLM, it creates a challenge where it is difficult to discern which information is useful and which is not useful.

Learners may learn the wrong approach


## Reference

1. [When LLMs Hallucinate: Examining the Effects of Erroneous Feedback in Math Tutoring Systems](https://www.researchgate.net/publication/394147567_When_LLMs_Hallucinate_Examining_the_Effects_of_Erroneous_Feedback_in_Math_Tutoring_Systems)
2. [Managing Hallucination Risk in LLM-Generated Outputs](https://dl.acm.org/doi/10.1145/3816713.3820249)
3. [Hallucinations in Large Language Models for Education: Challenges and Mitigation](https://ijtle.com/issue-alldetail/hallucinations-in-large-language-models-for-education-challenges-and-mitigation)

## Other Potential Useful Reference
- [Potential risks of generative artificial intelligence integration into K-12 education: A scoping review](https://www.sciencedirect.com/science/article/pii/S2666920X26000226)
- [The Mirage of Knowledge: Analyzing the Roots and Impacts of LLM Hallucination in Education](https://zenodo.org/records/18707654)

