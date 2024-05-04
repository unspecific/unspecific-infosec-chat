# unspecific-infosec-chat
Project in python to crate a chatbot that uses an LLM as the content creator.  Hallucinations expected

# Purpose
Drive engagement with employees around information security training.
Set up chat channel on a server such as Slack or Discord.  
Announce the AI chatbot os there to answer any infosec questions.
Every 4 hours the InfoSec Chatbot will post random infosec advice.
Remind everyone that AIs make mistakes and hallucinate
Announce you will give a reward to the first person who spots a mistake in one of the chatbots advice posts 

Let's me practice python on something fun.

Based on a silly idea that started on Twitter.
<https://twitter.com/unspecific/status/1786144355847217489>



This project will use MacOS for the initial build. 
It will also be designed to work on Linux.
The initial LLM it will build with will be ollama with 
llama3:latest             	a6990ed6be41

This will run as a stand alone process that connects to the specified LLM and a UI interface.  
Will be able to connect to Discord and Slack 

## Experiment
One of the things I wll be trying to having th LLM police itself for what it is saying.
We will ask the LLM to verify the content it creates and ask it to rewrite it with being easier to understand.
It will also be used to verify if the question is appropriate before it answers.



## Basic workflow:
    Connect LLM
        Setup API connection to designated LLM
        Initiate "personality"
    Connect to UI
        Setup API interface to service to interact with
    Listen
        Wait for input on channel ( must be tagged @'d )
        Generate Content
        Cleanup Content
    Timer
        Based on config at a designated time, the script will ask the LLM to generate content.
            Predefined personalities and prompts
            Custom - config driven
        LLM responds with content.
        Cleanup content
    Cleanup Content
        Content sent back to LLM a few times to get the right content to share
        Content sent to sharing 


Bot will track some internal history from the channel.
