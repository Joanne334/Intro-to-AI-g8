# Project Title

Personalized Mandarin Reading Learning Assistant 情勒橘子


## Project Description

[Enter a brief description of your project, including the data you used and the analytical methods you applied. Be sure to provide context for your project and explain why it is important.]

## Project Description

[Enter a brief description of your project, including the data you used and the analytical methods you applied. Be sure to provide context for your project and explain why it is important.]

## Getting Started

The codes for now can only run on Google Colab, you will need secrets of OpenAI's api key'OPENAI_API_KEY' and MongoDB URL 'MGDB_IAI'. 
Codes that can run on local devices are still under development.


To see the user interface and result, download and run `0525LLM(Peggy).ipynb` on Colab.any necessary software or data. Include installation instructions and any prerequisites or dependencies that are required.]

## File Structure

[Describe the file structure of your project, including how the files are organized and what each file contains. Be sure to explain the purpose of each file and how they are related to one another.]

## Analysis
#### Preprocessing
For preprocessing, texts including poems, children’s literature, and textbooks are extracted from various sources and converted into a standardized format.
This data is then segmented into sentences and tokenized using CKIP transformers to analyze the word and sentence levels.

#### Score levels
To quantify text difficulty, we employ NAER’s TOCFL levels. We will calculate an average proficiency score for each reading material by averaging the difficulty levels(1 to 7) of its constituent words. 

#### Employ RAG
The core of our methodology utilizes a RAG framework. We store pre-labeled text data and TOCFL word levels in MongoDB, which serves as a knowledge base for the LLM. The LLM can then adapt and rewrite original, high-difficulty texts such as classical literature like Dream of the Red Chamber into versions that are targeted to the user's required level.

#### Evaluation
For evaluation, we will call the LLM again to grade the level of the generated texts on different aspects, such as vocabulary and grammar level match, or how the generated text meaning aligns with the original text. 
We found that when the user's target level is low(1 or 2), the evaluation may score a higher level such as level 3 or 4. We assume that it is because some necessary vocabluaries have a higher level, but in order to align with original meaning, the LLM can't change the specific word, causing the average level higher than expected.
In the future, we'd like to compare how our RAG performes to general LLM performance, to show our project's distinctiveness.


## Results

Our suggestion of future reasearch is clear, that the realm of the difference in test performance of learning Mandarin with and without the assistance of AI can be further investigated. If we can further prove that there is a significant difference in test performance with the usage of this AI model, considering the learing incentives and the sentimental dynamics, we might have more space for improvement and stances to prove the effectiveness. 

## Contributors


| Name  | Labor |
| ------------- | ------------- |
| Joanna 113ZU1015 | data collecting, data cleaning  |
| Joanne 113ZU1013 | preprocessing, word labeling |
| Peggy 113ZU1009 | level labeling, text and quiz generation|



## Acknowledgments

We would like to thank Professor Pieng and teaching assistant Yo Yo for providing all-around help whilst designing and refining the whole framework. We initially would like to work on rewriting english content, catering to the english learners. Eventually, thanks for the advice of shifting the plan for foreigners learing Mandarin, we are now able to tackle the pain point that is less mentioned and resolved. 

## References

[List any references or resources that you used during your project, including data sources, analytical methods, and tools.]
