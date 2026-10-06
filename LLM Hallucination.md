# LLM Hallucinaton

## Executive Summary

## Problem

LLM is known to have hallucination problem since 2022. However, as models are getting better, the number of occurrences in hallucination reduces greatly. However, this does not mean that there will be no hallucination even in simple cases.  

Recently, I encounter a situation where LLM give me the wrong answer to a probability challenges. 

On a separate issue, when we ask LLM question, always as LLM for information source. Sometimes, the source may surprises you. 

On a separate assignment, we also learn that frontier model is good at extracting numbers from a table in image form, able to analyze chart in image form, and deciphering relative position on a map in image form. Frontier model is fairly good in detecting objects in an image provide the object is distinctive. However, frontier model failed in analyzing complex transit map and calculating the optimize route.  

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
When asking a question, always as for information source. In a recent exercise, we asked Gemini "What is the limitation of LLM". Gemini use search to gather results and compose a response with source link. Source link is provided because in my system prompt, we include an instruction to always include source of information.

![alt text](<assets/Screenshot 2026-10-05 at 13.11.17.png>)

You will be surprise that some source are from blog post. This does not meant that blog post is no good, but extra efforts is need to look at the source document to confirm the validity of the source.  

[Source of Gemini](https://share.gemini.google/xOjCs52VmWq7)


## Implications

- As independent learner who need a lot of help in Mathematics, we need to be careful on LLM reasoning on Mathematics.
- There is a need to re-calibrate the trust factor for LLM.
- Seems that LLM is bad in reasoning in Mathematics.
- If LLM are introduced as teaching assistant especially in school, it may caused more confusion.
- With a mix of reliable and unreliable information in LLM, it creates a challenge where it is difficult to discern which information is useful and which is not useful.


## Mitigation

- Use RAG when possible and ask LLM to indicate if the information is outside the RAG source truth.
- Use different LLM to verified answer. (As shown in problem above, we use Claude to verified the answer)
Explore the prompting technique Comparative and Cross-Verification Prompting (CCVP) mentioned in (https://ieeexplore.ieee.org/document/10645894/) 
- Query the same question multiple times. This is to make sure we get consistent response. (See  [5 Practical Techniques to Detect and Mitigate LLM Hallucinations Beyond Prompt Engineering](https://machinelearningmastery.com/5-practical-techniques-to-detect-and-mitigate-llm-hallucinations-beyond-prompt-engineering/))
- Other techniques not relating to mathematics include adding an instruction to always provide information source when stating facts.This is to allow learner to make sure that the information source is trustworthy.
- For getting trust worthy source of information, we can always constraint the LLM from getting answers from papers instead of internet. 


## Conclusion

- This exercise reinforce the notion that LLM is not good at reasoning.
- We need to recalibrate our trust factor if we are too trusting previously.
- Be aware of which area did LLM hallucinates heavily.
- When asking Mathematical question and any question that requires reasoning, be extra vigilant to counter check with multiple sources.
- If LLM is not good at reasoning, then why LLM score well in Mathematics benchmark? Is Goodhart Law at play? (Open for discussion)


## Reference

1. [When LLMs Hallucinate: Examining the Effects of Erroneous Feedback in Math Tutoring Systems](https://www.researchgate.net/publication/394147567_When_LLMs_Hallucinate_Examining_the_Effects_of_Erroneous_Feedback_in_Math_Tutoring_Systems)
2. [Managing Hallucination Risk in LLM-Generated Outputs](https://dl.acm.org/doi/10.1145/3816713.3820249)
3. [Hallucinations in Large Language Models for Education: Challenges and Mitigation](https://ijtle.com/issue-alldetail/hallucinations-in-large-language-models-for-education-challenges-and-mitigation)

## Other Potential Useful Reference
- [Potential risks of generative artificial intelligence integration into K-12 education: A scoping review](https://www.sciencedirect.com/science/article/pii/S2666920X26000226)
- [The Mirage of Knowledge: Analyzing the Roots and Impacts of LLM Hallucination in Education](https://zenodo.org/records/18707654)
- [How Accurate Is ChatGPT for Math?](https://99helpers.com/blog/how-accurate-is-chatgpt/for-math)
- [Hallucination detection, verification, and correction in generative AI: A comprehensive survey](https://www.sciencedirect.com/science/article/pii/S2949719126000361)


