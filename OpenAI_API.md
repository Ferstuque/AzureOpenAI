# 🚀 Azure OpenAI API Guide

This guide contains information about the main features of API **Azure OpenAI**, including *Chat, functions, scripts, configurations, Kernel Semantic**, and more.

## 📌 API Overview

Azure OpenAI provides access to several powerful AI capabilities:

- **💬 Chat** – Interact with OpenAI's models using conversational AI.
- **✍️ Completion** – Generate text based on a given prompt.
- **🖼️ Image Generation** – Create images using DALL·E models.
- **🎵 Audio Processing** – Convert speech to text and vice versa.
- **🧮 Code Interpreter** – Perform calculations and run code.
- **🌍 Translation** – Translate text into different languages.

---

## 🛠️ API Configuration

To use the Azure OpenAI API, configure your client:

```python
from openai import AzureOpenAI
import os

client = AzureOpenAI(
    azure_endpoint=os.getenv("AZURE_OPENAI_ENDPOINT"),
    api_key=os.getenv("AZURE_OPENAI_API_KEY"),
    api_version="2024-02-01"
)
```

---

## ✍️ Completion API

Generate text from a prompt:

```http
POST https://{endpoint}/openai/deployments/{deployment-id}/completions?api-version=2024-10-21
Content-Type: application/json
Authorization: Bearer {api_key}

{
 "prompt": [
  "Tell me a joke about mango"],
 "max_tokens": 32,
 "temperature": 1.0,
 "n": 1
}
```

📌 **Docs**: [Azure OpenAI Completion API](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/completions)

---

## 💬 Chat API

Interact with chat models:

```python
messages = [
    {"role": "system", "content": "You are a helpful assistant."},
    {"role": "user", "content": "Tell me a fun fact about space."}
]

response = client.chat.completions.create(
    model=os.getenv("AZURE_OPENAI_DEPLOYMENT_NAME"),
    messages=messages,
    temperature=0.7
)
```

📌 **Docs**: [Azure OpenAI Chat API](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/chat-completions)

---

## 🎨 Image Generation API

Generate images using DALL·E:

```python
response = client.images.generate(
    model="dall-e-3",
    prompt="A futuristic city skyline at sunset",
    n=1,
    size="1024x1024"
)
```

📌 **Docs**: [Azure OpenAI Image API](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/image-generation)

---

## 🎵 Audio API (Speech-to-Text & Text-to-Speech)

Convert speech to text:

```python
response = client.audio.transcriptions.create(
    model="whisper-1",
    file=open("speech.mp3", "rb")
)
```

📌 **Docs**: [Azure OpenAI Speech API](https://learn.microsoft.com/en-us/azure/ai-services/speech-service/)

---

## 🔢 Common API Parameters

- **Model ID** – Specifies which model to use.
- **Temperature** – Controls randomness in responses.
- **Max Tokens** – Limits the length of the response.
- **Top P** – Nucleus sampling for response variation.
- **Presence/Frequency Penalty** – Adjusts response repetition.

Example usage:

```python
response = client.completions.create(
    model="gpt-4",
    prompt="Write a short poem about the ocean",
    max_tokens=50,
    temperature=0.8,
    top_p=0.9
)
```

---

## 🧠 Kernel Semantic (SK) Overview

![Semantic Kernel](https://learn.microsoft.com/en-us/semantic-kernel/media/sk-overview.png)

📌 **Docs**: [Semantic Kernel Overview](https://learn.microsoft.com/en-us/semantic-kernel/)

### 🔧 Key Features:

- **🛠️ Functions** – Encapsulate reusable logic.
- **🤖 AI Agents** – Use AI to automate tasks.
- **📚 Skills** – Modular capabilities for AI tasks.
- **🧠 Memory** – Store & retrieve context.
  - **📂 Vector Stores** – Store embeddings for retrieval.
  - **🔍 API Search** – Quickly find relevant data.
- **🛡️ Filters** – Customize AI behavior.
- **🖥️ SDK Demo** – Run prebuilt examples.

📌 **Docs**: [Semantic Kernel SDK](https://learn.microsoft.com/en-us/semantic-kernel/quickstart/)

---

## 📚 Additional Resources

- [🔗 Azure OpenAI Documentation](https://learn.microsoft.com/en-us/azure/ai-services/openai/)
- [🔗 OpenAI API Reference](https://platform.openai.com/docs/api-reference)
