## Dummy Agent Project

This is a minimalistic, framework-agnostic project that demonstrates how to simulate an AI Agent using Hugging Face's serverless inference API. The project uses the Meta-Llama-3-8B-Instruct model to create an interactive agent capable of structured reasoning and tool use, despite not being integrated with real APIs. It is a dummy project and the Agent is not provided with a working tool.

## Overview
The Dummy Agent mimics how large language models can interact with external tools using a structured Thought → Action → Observation → Answer format. In this project:

- A dummy tool get_weather(location) is defined.

- The model generates a structured reasoning trace to decide when to use the tool.

- Tool usage is simulated manually via a Python function.

- The model then proceeds with its final answer using the "observed" result.

## Requirements
Install the necessary package:

pip install -q huggingface_hub -U

## Setup
- Get your Hugging Face Token via: https://hf.co/settings/tokens

- Generate a token with read access.

- Copy the token.

- Apply for access to the Meta Llama 3 model

- Visit: https://huggingface.co/meta-llama/Meta-Llama-3-8B-Instruct

- Fill out the request form (access might take time).

- Authenticate the Inference Client


## Limitations
- The tool (get_weather) is simulated with a static function. No real-time API is called.

- The model may hallucinate Observations if not stopped at the right point.

- Multi-turn reasoning is simulated manually, not autonomously handled.

