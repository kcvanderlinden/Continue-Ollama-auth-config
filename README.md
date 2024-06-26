# Continue-Ollama-auth-config
A configeration for using Ollama in VSCode with API Authentication

## Setting Up Continue in VSCode with an Ollama Server Using Caddy Authentication

This repository provides a configuration guide to set up Continue in Visual Studio Code (VSCode) with an Ollama server that uses Caddy for authentication. The setup includes detailed instructions on how to configure the environment and where to place certain files.

### Prerequisites
- **Ollama Server**: Ensure you have an Ollama server running and accessible via API.
- **Caddy Server**: Set up a Caddy server with appropriate authentication configurations. See my other repo for a simple setup: [ollama-caddy-authentication](https://github.com/kcvanderlinden/ollama-caddy-authentication)
- **VSCode**: Install Visual Studio Code on your machine if it's not already installed.
- **Continue**: Install Continue in Visual Studio Code (VSCode) if it's not already installed.

### Configuration Steps

**Configure API Authentication**:
- Change the `config.json` file in the directory `C:/users/<your username>/.continue/config.json`. This file can also be accessed from within the Continue extension in VSCode (click on continue icon in your right bar > click on the settings icon in the chat overlay right below) Copy the content from the config.json in this repo and change the variables between <> with your API authentication key and the address of you Ollama endpoint.
- Change the settings.json file of VSCode. This file can be accessed by hitting Ctrl+Shift+P and searching for 'Preferences: Open users settings (JSON)'. Copy the content from the settings.json file from this repo to the end of the file between the curly brackets '{}'.Change the variables between <> with your API authentication key and the address of you Ollama

**Specifiy the models you want to use**
- As an example, Deepseek-coder-v2 (:16B) and starcoder2 (:3B) are two models that I have choosen to use with my Ollama server (running an RTX 3060). Change the models variable between <> with the model names you want to use. However, using a different model then the one specified in the config file can result in wrong output. You then also could change the template per model (see: [template config](https://docs.continue.dev/setup/configuration#customizing-the-chat-template))