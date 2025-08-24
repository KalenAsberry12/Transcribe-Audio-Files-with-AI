<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Transcribe Audio Files with AI

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-ai-transcribe)

**Author:** Kalen Asberry  
**Email:** kalenasberry52@gmail.com

---

![Image](http://learn.nextwork.org/secure_red_beautiful_frog/uploads/aws-ai-transcribe_o2p3q4r1)

---

## Introducing Today's Project!

# 

In this project, audio data is everywhere, from podcasts and lectures to customer service calls and voice notes. Being able to automatically transcribe this data opens up a world of possibilities imagine turning every audio file into searchable text, subtitles, or blogs! In this project, you'll gain hands-on experience with transcribing videos and audio using AWS services.

### Tools and concepts

Services I used were Amazon S3 for video stprage and Amazon Transcribe for transcription. Key concepts I learnt include live transcribingm custom vocabularies and filtersm Transcibe <> S3's connection. 

### Project reflection

his project took me approximately 1.5 hours including demo time. The most challenging part was creating the custom vocabulary. It was most rewarding to do a live transcript and see the custom vocab + filter at work straight away!

I did this project to learn about transcirption and AI tools like transcribe! This project helped meet me goals of letting me practice transcription + ways to make it even mroe accurate.

---

## S3 and Transcribe

To set up for this project, I'm using an S3 bucket to store the video file that we're transcribing. The file we're transcibing is a 1 minute clip of an existing project demo. This is a great opportunity to provide subtitles to our videos!

![Image](http://learn.nextwork.org/secure_red_beautiful_frog/uploads/aws-ai-transcribe_k1l4m7n0)

---

## Run A Transcription Job

The Steps to run a transcription job include selecting a language and model type; selecting input and output data (i.e where the video/audio is from, and where the transcription should be stored)/ Overall, this process took us about 5 minutes.

Amazon Transcribe uses model types to learn how to translate speech to text. You can think of a model type as an instruction or guide that Transcribe uses. use cases of model types include creating custom models for medical/legal conversations.

Wecan customise a transcription further with subtitling, which adds subtitles to a video (great for accessibility or translations);  and speaker partitioning, which helps to identify multiple speakeres in a audio file.

![Image](http://learn.nextwork.org/secure_red_beautiful_frog/uploads/aws-ai-transcribe_g0h1i2j3)

---

## Baseline Transcript Review

To start using Amazon Transcribe, we first ran a baseline transcription job, which mwans a transcription that doesn't use any of the additional features ortools provided by amazon Transcribe. This lets us compare the results of any changes.

Whike reviewing the baseline transcription, we noticed a few inaccuracies, including typos (e.g. 'repositories' spelt as 'repositoriesies',) jargon (e.g. '403 Forbidden' transcibed as '4 or 3 forbidden'), filler words (e.g. 'um') and lack of context/

![Image](http://learn.nextwork.org/secure_red_beautiful_frog/uploads/aws-ai-transcribe_s3t6u9v2)

---

## Custom Vocabulary

I can resolve transcription inaccuarcies using a custom vocabulart, which is a defined list of technical  or mispelt words that we want Transcribed to process accurately. understand and transcribe accurately. A custom vocabulary impoves accuracy by defining the correct transcription.

To create an item in a custom vocabulary, you need to define two values. They are 'phrase'm which means the phrase we want Transcibe to detect; and  'DisplayAs', which is the way we want Transcribe to display the words in its transcriptions.

My custom vocabulary defines the proper spelling/treatment of three inaccuracies in out baseline transciption. First, 'player -> 'Player'. Second, '4 or 3 forbidden -> '403 Forbidden'. Third, 'repositoriesies' -> 'repositories'.

![Image](http://learn.nextwork.org/secure_red_beautiful_frog/uploads/aws-ai-transcribe_e3f4g5h6)

---

## Vocabulary Filters

Another feature in Transcribe is vocabulary filtering, which is a tool for removing unwanted words.  It's different from custom vocabularies - vocabularies are used for words we Do want to transcribe (accurately), whereas filterd words aren't wanted. 

My vocabulary filter removes unwanted text, like filer words ('um') To set up this filter, I first created a filter file, which is a comma separated list of words

![Image](http://learn.nextwork.org/secure_red_beautiful_frog/uploads/aws-ai-transcribe_u7v8w9x0)

---

## Enhanced Transcription

### I ran a new transcription with my custom vocabulary and filtering settings

The enhanced transcription is better than the baseline because it does not have the same typos; it's now capitalised 'player' to turn into a title, and filler words are correctly identified and masked! We'll need more training to fix the '403' error

![Image](http://learn.nextwork.org/secure_red_beautiful_frog/uploads/aws-ai-transcribe_k1l2m3n4)

---

## Real Time Transcription

For my project extension, I experimented with real-time transcription, which is transcription that happens live while the speaker is still talking. This is helpful for apps that want to deliver live captioning or voice commands.

Even during real-time transcription, I could use features like cocabylary filtering and custom vocabulary. Overall, compared to a transcription job, real-time transcription was still just as accuarate. Although '403 forbidden' still has errors.

![Image](http://learn.nextwork.org/secure_red_beautiful_frog/uploads/aws-ai-transcribe_a5b6c7d8)

---

---
