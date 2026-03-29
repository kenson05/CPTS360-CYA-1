# Reflection

## Activity Description
I built a real time translation system for my local Korean church.

My local church used to offer English translation through Zoom with a volunteer reading off a translated version of the script. They had two main issues they were dealing with. First the quality of the translation was not good as the pastor oftentimes went deeper into things not written in the script causing the translation to be very inconsistent. Second they would have trouble finding volunteers every week resulting in no translations on certain weeks especailly during breaks. I proposed an idea to make a web app that translated the sermon in real time using AI. The pastor liked the idea and I was able to deploy the software and the church has been using it every Sunday for the past couple of months. Every week I am updating the software with new features and bug fixes.

## Technical Decisions
I created a web application using React and Node.js that allows the pastor to create a session for his sermon and input the sermon audio either through a microphone or directly from the church audio system. I used the Deepgram API for transcription as they gave a very generous amount of free credits and I used OpenAI's gpt-40-mini model for translation along with their tts-1 model for text-to-speech. I used Prisma and PostgreSQL for the data base and the project was deployed using Railway. 

## Challenges
I faced many challenges while building this project however the hardest one I dealt with was finding the right balance between latency and accuracy and also debugging the translation pipeline. 

Early on I faced challenges with the pipeline occasionally skipping or outputting the wrong outputs. Since nothing was explicitly breaking I was left confused on what was causing the error. I was able to fix this by adding logs throughout the pipeline along with error messages which allowed me to narrow down where it was breaking and was able to fix the issues. One example was certain audio chunks being too short for transcription causing an empty message being sent to the translation model, resulting in a response that was incorrect. 

Another challenge was finding the balance between having short transcriptions which allowed for faster translations but a less accurate one. However longer transcriptions took longer to process but resulted in more accurate results. I was able to find a good balance where I set the boundary to around 2 sentences per chunk, which allows for near real-time speed along with accurate translations.

## Contributions
I built this application end-to-end by myself. I leveraged AI to help me design the system architecture and help develop the front end.

## Career Alignment
This project aligns with my goals for the future because I want to become a software engineer that helps tackle real-world problems using AI. Being able to have meetings with the church members and getting feedback helped me learn how important it is to build the software for the people actually using it rather than making all of the decisions on my own. Through this project I have learned a lot on what it takes to build a system that will be used by real people compared to course projects. For example deployment is not something that is expected in a lot of course projects however for real life systems it is one of the most important parts.

Overall this was a big learning experience for me and I hope to translate what I learned from this project into future projects and work.
