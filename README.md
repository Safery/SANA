# SANA!

Hi! what is **SANA** you ask..? She is an automated text to speech AI that can read sentences or text with expression. SANA can understand the difference between "angry", "emotional" scenario in a given text which she will use to create that voice to read the text aloud. 

Text to Speech generation nowadays are done via one singular tone. There are no expression and it sounds very robotic. SANA on the other hand is 100% robotic but the way she manipulates her voice to create "fake" emotion is what matters and makes it sound realistic.

```mermaid
graph LR
A[String] -- POST --> B[Processing the text for emotion]
B -- POST --> C[SANA receives processed text and generates response]
C -- POST --> D[Text 2 Speech Generation]
```

### Example
Given the following String with different 'text' tones, SANA will produce different voice expression: `hi, my name is Sana`.
|                |Text Tones                          |Sana Expression                         |
|----------------|-------------------------------|-----------------------------|
|All Capital|`'HI! MY NAME IS SANA'`            |<low pitch, heavy enthusiasm>            |
|Sad expression          |`hi... my name.. is Sana..`            |<high pitch, quiet voice with many uncertainty>            |
|Excited Expression          |`Hi! My name is Sana!`|<mid pitch, fast break time> |


# General Overview

### What is TTS (Text 2 Speech)?
Text to speech (TTS) is a natural language modeling process that requires changing units of text into units of speech for audio presentation. This is the opposite of speech to text, where a technology takes in spoken words and tries to accurately record them as text. Text to speech is now common in technologies that seek to render audio output from digital text to assist those who are unable to read, or for other kinds of uses.

Developing text-to-speech capability includes some unique challenges. Especially in the English language, where a great number of homonyms have varied pronunciations, computer programs rely on probability modeling to guess the desired pronunciation of a word in digital text. The program also has to convert units of text into phonemes, the smallest units of speech pronunciation. The result is that many text-to-speech technologies are less than infallible, although SANA will be expressible ;)

![alt text](https://i.imgur.com/LOAbmcN.png)

### Benefits of SANA
While text to speech has benefits for all users, some of the specific groups that see a better user experience are:
- **People with learning disabilities**
- **People who have literacy difficulties**
- **People who speak the language but do not read it**
- **People who multitask**
- **People who multitask**
- **People who access content on mobile devices**
- **People with different learning styles**

### Test of SANA
We can evaluate the expression of SANA with MOS model. MOS gives a numerical indication of the quality of the synthesized speech. In this method, focus of evaluator should be on naturalness of synthetic speech. By Naturalness it is meant that the sound is indistinguishable from human speech and it is close to human voice.

$$
MOS =  \frac{ \sum_{j=1}^M ( \frac{ \sum_{i=1}^N  S_{ij}  }{N} ) }{M} 
$$

S(i) Score of i'th evaluator 
N = # of Evaluators 
M = # of Sentences 
j = Sentence Index

Given the output of formula above where MOS > 0 and < 6, where 5 is Excellent expression and 1 being very robotic.
