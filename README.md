

# Llama3 and Gemma Model Setup Instructions

## Youtube recording link
https://youtu.be/d01A1caYCG8
https://youtu.be/X_S02HiaP20

## Prerequisites

1. **Download the Ollama App:**
   - You can find it [here](https://github.com/Ollama/ollama) or use the direct links below:
     - [Download for Mac](#) (This link will automatically start downloading for macOS)
     - [Download for Windows](#) (This link will automatically start downloading for Windows)

2. **Install the Ollama App:**
   - Open the Ollama app and follow the instructions on the screen to complete the installation.

## Setting Up Llama3 Model

1. **Run the Llama3 Model:**
   - Open your terminal and execute the following command:
     ```bash
     ollama run llama3
     ```
   - This process might take a few minutes.

2. **Interact with Llama3:**
   - You can prompt questions in the shell. For example:
     ```shell
     Why the banana is yellow?
     ```
   - To quit the conversation mode, type:
     ```shell
     /bye
     ```

3. **Use `curl` Commands to Interact with the Model:**
   - To send a prompt using `curl`, use the following command:
     ```bash
     curl http://localhost:11434/api/generate -d '{
       "model": "llama3",
       "prompt": "Why the banana is yellow?"
     }'
     ```
   - The response will be split into single words and sent back to you in many lines of JSON.

4. **Disable Streaming Response:**
   - If you prefer to receive the response all at once instead of in a stream, use this command:
     ```bash
     curl http://localhost:11434/api/generate -d '{
       "model": "llama3",
       "prompt": "Why the banana is yellow?",
       "stream": false
     }'
     ```

## Setting Up Gemma Model

1. **Run the Gemma Model:**
   - Open your terminal and execute the following command:
     ```bash
     ollama run gemma:2b
     ```
   - This process might take a few minutes.

2. **Interact with Gemma:**
   - The steps are similar to the Llama3 model. You can prompt questions in the shell and quit the conversation mode using `/bye`.

3. **Use `curl` Commands to Interact with Gemma:**
   - To send a prompt using `curl`, use the following command:
     ```bash
     curl http://localhost:11434/api/generate -d '{
       "model": "gemma:2b",
       "prompt": "Why the banana is yellow?"
     }'
     ```
   - To disable the streaming response, use this command:
     ```bash
     curl http://localhost:11434/api/generate -d '{
       "model": "gemma:2b",
       "prompt": "Why the banana is yellow?",
       "stream": false
     }'
     ```


