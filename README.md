# Choose Your Own Adventure 01

**Kenneth Son**<br>
WSU ID: 11861711


## Adventure Overview
I built a real time translation system for my local Korean church.<br><br>My local church used to offer English translation through Zoom with a volunteer reading off a translated version of the script. They had two main issues they were dealing with. First the quality of the translation was not good as the pastor oftentimes went deeper into things not written in the script causing the translation to be very inconsistent. Second they would have trouble finding volunteers every week resulting in no translations on certain weeks especailly during breaks. I proposed an idea to make a web app that translated the sermon in real time using AI. The pastor liked the idea and I was able to deploy the software and the church has been using it every Sunday for the past couple of months. Every week I am updating the software with new features and bug fixes. 

## Career Goals
My future career goal is to become a software engineer that builds real world, impactful software that helps people. I also have an interest in the applications of AI and how it will change the world in the future.

This project aligns with my goals by: 

- Applying AI tools to solve real user problems
- Designing and implementing a full-stack system
- Building a product with potential for real-world deployment and scalability.

## Project Description
The system processes live audio input from sermons and translates it through a pipeline of speech recognition and translation services before displaying the output to users on their mobile devices.

## Tech Stack (High Level)
Frontend: React + Typescript

Backend: Node.js

Speech-to-Text: Deepgram API

Translation: OpenAI API

Data Handling: JSON-based streaming and processing

Deployment: Railway

## System Architecture
The application follows a streaming pipeline architecture:

Audio Input → Speech-to-Text (Deepgram) → Translation (OpenAI) → Frontend Display

- Audio is captured and streamed to Deepgram for Korean transcription
- Transcribed text is processed and sent to OpenAI for translation
- The translated output is displayed to the user in real time on their mobile device 
- The output can be viewed as a transcription or listened to through TTS

## Deliverable
Due to plans onreleasing the software to the public and potentially commercializing it, I have decided not to share the source code. However screenshots of the application can be found in the `assets/` folder.

## Reflection
See `reflection.md`.
