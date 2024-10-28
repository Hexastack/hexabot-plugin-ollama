# Ollama Plugin Extension for Hexabot AI Chatbot / Agent Builder

## Overview

The Ollama Plugin Extension is a custom block for the Hexabot Chatbot / Agent Builder that introduces Generative AI and Retrieval-Augmented Generation (RAG) capabilities. This plugin allows you to enhance your chatbot with cutting-edge AI features, providing more context-aware and intelligent responses by leveraging generative models and document-based retrieval.

[Hexabot](https://hexabot.ai/) is an open-source chatbot / agent solution that allows users to create and manage AI-powered, multi-channel, and multilingual chatbots and/or agents with ease. If you would like to learn more, please visit the [official github repo](https://github.com/Hexastack/Hexabot/).

## Features

- **Generative AI Capability**: Leverage state-of-the-art language models, such as Llama 3.2, to generate human-like responses for your chatbot.
- **RAG Integration**: Combine generative models with retrieved content from the Hexabot Knowledge Base to provide grounded responses based on managed documents, enhancing both accuracy and relevance.
- **Customizable Settings**: Modify model parameters, control context length, adjust temperature, and customize system instructions for fine-tuned behavior.

## Plugin Settings

The plugin offers a wide range of customizable settings, grouped into two categories: `default` and `options`. These settings allow you to fine-tune the behavior of the generative AI to meet specific needs.

### Default Settings
- **Model** (`text`): Specifies the language model used. Default is `llama3.2`.
- **Keep Alive** (`text`): Duration to keep the model in memory. Default is `5m`.
- **Max Context Messages** (`number`): Number of messages to retrieve for contextual conversations. Default is `5`.
- **Context** (`text`): A context description for the AI. Default is: "You are an AI Assistant that works for Hexastack, the IT company behind Hexabot the chatbot builder."
- **Instructions** (`textarea`): Custom instructions to guide the AI responses. 
- **Fallback Message** (`textarea`): Message to send when an error occurs.

### Optional Settings
- **Mirostat** (`number`): Mirostat tuning. Default is `0` (disabled).
- **Mirostat Eta** (`number`): Mirostat eta parameter. Default is `0.1`.
- **Mirostat Tau** (`number`): Mirostat tau parameter. Default is `5.0`.
- **Context Window Size** (`number`): Maximum number of tokens for the model's context window. Default is `2048`.
- **Repeat Last N** (`number`): Number of tokens to consider for repetition penalty. Default is `64`.
- **Repeat Penalty** (`number`): Penalty for repeated phrases. Default is `1.1`.
- **Temperature** (`number`): Sampling temperature for response variability. Default is `0.8`.
- **Seed** (`number`): Seed value for deterministic outputs. Default is `0`.
- **Stop** (`text`): Stop sequence for model output. Default is `"AI assistant:"`.
- **TFS Z** (`number`): TFS Z value (top fractional sampling). Default is `1.0`.
- **Maximum number of tokens** (`number`): Maximum number of tokens to predict. Default is `20`.
- **Top K** (`number`): Top-k sampling value. Default is `40`.
- **Top P** (`number`): Top-p sampling value. Default is `0.9`.
- **Min P** (`number`): Minimum probability for sampling. Default is `0.0`.

## Installation

1. Install the plugin package using:

```sh
cd ~/projects/my-chatbot
npm install hexabot-plugin-ollama
hexabot dev --services ollama
```

## Usage

After installing and registering the plugin, the Ollama block will be available in the visual editor of Hexabot. You can drag and drop the Ollama block into your chatbot's workflow to add generative AI + RAG capabilities. Configure the settings through the block to customize the model and behavior.

This plugin utilizes document-based retrieval from the Knowledge Base to enhance responses, which means your chatbot can leverage specific documents to generate more relevant answers. You can find more about the Knowledge Base in the official documentation : https://docs.hexabot.ai/user-guide/knowledge-base


## Contributing

We welcome contributions from the community! Whether you want to report a bug, suggest new features, or submit a pull request, your input is valuable to us.

Please refer to our contribution policy first : [How to contribute to Hexabot](./CONTRIBUTING.md)

[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](./CODE_OF_CONDUCT.md)

Feel free to join us on [Discord](https://discord.gg/rNb9t2MFkG)

## License

This software is licensed under the GNU Affero General Public License v3.0 (AGPLv3) with the following additional terms:

1. The name "Hexabot" is a trademark of Hexastack. You may not use this name in derivative works without express written permission.
2. All derivative works must include clear attribution to the original creator and software, Hexastack and Hexabot, in a prominent location (e.g., in the software's "About" section, documentation, and README file).

---

_Happy Chatbot Building!_
