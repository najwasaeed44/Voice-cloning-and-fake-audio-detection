
[//]: # (____________________________________PROJECT TITLE____________________________________)

<br>

<h1 align="center">
  <img src="https://github.com/najwasaeed44/data-science-project-theme/blob/main/img/logo.png?raw=true" width="200px"/><br/>
Voice Cloning and Fake Audio Detection
</h1>


<hr style="height:4px;border-width:10;color:blue;background-color:black">


<br><br><br><br>

[//]: # (____________________________________BACKGROUND____________________________________)

<img src="https://images.genial.ly/59e059d30b9c21060cb4c2ec/5bbf17763292ef649e9b810f/175cbb1e-df65-405a-9cd0-cf177e1a2f00.gif?genial&1633910400074" width="60" height="70" align="left">

## Background:
<hr style="height:1.5px;border-width:10;color:blue;background-color:black">


We are a technology company working in the Cyber Security industry. We focus on building systems that help individuals and organizations to have safe and secure digital presence by providing cutting edge technologies to our customers. We create products and services that ensure our customers security using data driven technologies to understand whether audio and video media is authentic or fake.


Our goal in this project is to build algorithms that can synthesize spoken audio by converting a speaker’s voice to another speaker’s voice with the end goal to detect if any spoken audio is pristine or fake.

<br><br>


[//]: # (____________________________________DATA DESCRIPTION____________________________________)


<img src="https://media.baamboozle.com/uploads/images/67969/1595412283_471863"  width="60" height="70" align="left">

## Data Description:
<hr style="height:1.5px;border-width:10;color:blue;background-color:black">

There are two datasets you can utilize in this project. Both datasets are publicly available sources.


- TIMIT Dataset:


The TIMIT corpus of read speech is designed to provide speech data for acoustic-phonetic studies and for the development and evaluation of automatic speech recognition systems. TIMIT contains a total of 6300 sentences, 10 sentences spoken by each of 630 speakers from 8 major dialect regions of the United States.


Dataset Link: https://github.com/philipperemy/timit


- CommonVoice Dataset:


Common Voice is part of Mozilla's initiative to help teach machines how real people speak. Common Voice is a corpus of speech data read by users on the Common Voice website (https://commonvoice.mozilla.org/), and based upon text from a number of public domain sources like user submitted blog posts, old books, movies, and other public speech corpora. Its primary purpose is to enable the training and testing of automatic speech recognition (ASR) systems.


Dataset Link: https://commonvoice.mozilla.org/en/datasets

<br><br>


[//]: # (____________________________________COAL____________________________________)

<img src="https://c.tenor.com/1_5w5vXEH5gAAAAj/mandalorian-star-wars.gif" width="60" height="60" align="left">

## Goal(s):
<hr style="height:1.5px;border-width:10;color:blue;background-color:black">


Build a machine learning system to detect if a spoken audio is synthetically generated or not. In order to achieve this, first, build a voice cloning system given a speaker’s spoken audio that clones the source speaker’s voice to the target speaker’s voice. Next, build a machine learning system which detects if any spoken audio is a natural speech or synthetically generated by machine.

<br><br>

[//]: # (____________________________________PROJECT OVERVIEW____________________________________)


<img src="https://media0.giphy.com/media/LmqdA28jZ7bitDeDWr/200.webp"  width="60" height="60" align="left">

## Project Overview:
<hr style="height:1.5px;border-width:10;color:blue;background-color:black">

### 1) Experimentation with the audio cloning with four different techniques:

- Short Audio with a short text
- Short Audio with a long text.
- Long Audio with a short text.
- Long Audio with a long text.

Before explaining each technique, we need to know that, in the TIMIT data we have train and test data, in each dataset we have **168** speakers with 10 short audio files **(around 4s)**. 

In `"Short Audio with a short text"`, the original files have been cloned with one short sentence, and in `"Short Audio with a long text"`, the same files have been cloned but with two-sentence instead of one to have a longer sentence and to see how the cloning model will works.

On the other hand, both the `"Long Audio with a short text"` and `"Long Audio with a long text"`, are using different versions of the audio files. As mentioned before, we have **168** speakers which mean **336** in total. Each speaker's audio files have been merged into one file and cloned later. Both of the techniques use a short sentence and a longer one to see how the cloning model will work. Here are three samples that are used in the long audio version:

### 2) Voice Cloning:
After cloning three samples in each technique, the third one has been chosen -Long audio with a short sentence- and all of the **336** files have been cloned and saved.

The third technique has been chosen based on how accurate the model is to convert the text to speech. This was done by converting the cloned audio to the text again and calculating the similarity between the original text and the one from the cloned audio.

### 3) The Classifier:















<br><br>


[//]: # (____________________________________ CONCLUSION____________________________________)

<img src="https://media4.giphy.com/media/MbMUCH4MUffka1ZFeT/giphy.gif?cid=790b7611040baf4e7332c491694685e3367d8fe931cd7a69&rid=giphy.gif&ct=s"  width="80" height="60" align="left">

## Conclusion:
<hr style="height:1.5px;border-width:10;color:blue;background-color:black">

Different model hyperparameters were tested and in general, some of the models prefer well in the range of **10** epochs. From the training and optimization section, it's clear this data prefer a learning rate of around 0.001 and tanh activation function better than relu. Our best model test score is `99.7%` with a loss equal to `0.046`.

