EN
# Azure Open AI - Features

This repository contains information about the main features of Azure Open AI, including LLMs, models, tokenization, and more.

## LLMs (Large Language Models) 💡

**LLMs (Large Language Models)** are deep learning models trained with large volumes of text to generate, understand, and process human language.

LLMs are the key component behind text generation. In a nutshell, they consist of large pretrained transformer models trained to predict the next word (or more precisely, the next token) based on input text. Since they predict one token at a time, more elaborate processes are needed to generate new sentences beyond simply calling the model — **autoregressive generation** is required.

- **What are they?** They are neural networks that can perform a wide range of tasks, such as translation, text generation, summarization, etc.
- **In a nutshell:** They "learn" from large datasets and apply that knowledge to a variety of language tasks.

Learn more: [LLM Tutorial on Hugging Face](https://huggingface.co/docs/transformers/llm_tutorial)

## Open AI Tokenization 🔑

**Tokenization** is the process of splitting text into smaller units called *tokens*. These tokens can be words, parts of words, or even individual characters. OpenAI uses tokenization to efficiently understand and process text.

## Playground 🛠️

The **OpenAI Playground** provides an interactive interface to test language models with various parameters. Some key options are:

### Temperature 🌡️
- **What is it?** It controls the randomness of the generated responses.
  - **Temperature 0 to 1**: More deterministic or more creative responses.

### Top P 🎯
- **What is it?** An alternative method to control randomness, using a probabilistic approach to choose words.
  - **Top P from 0.1 to 0.9**: The cumulative probability of selected words.

### Max Tokens 🧑‍💻
- **What is it?** Limits the number of tokens generated in a response.

### Penalties ⚖️
- **Frequency Penalty**: Reduces excessive repetition of words.
- **Presence Penalty**: Penalizes the repetition of already used terms, increasing response diversity.

### Message System 💬
- **What is it?** Allows interaction with the model in a sequence of messages, useful for creating conversations or more contextual prompts.

### Prompt Engineering 📝
- **What is it?** The art of structuring prompts in a way that helps the model better understand what is being asked.

## Open AI Models 🧠

OpenAI offers several models for different purposes:

- **GPT-3 (gpt-3.5, gpt-3.5-turbo)**: General-purpose language models.
- **GPT-4**: The most advanced version with greater comprehension and generation capabilities.
- **GPT-1 Mini**: A compact and optimized version of GPT-1.
- **GPT-4 Turbo**: An optimized version of GPT-4, offering faster performance and reduced costs.
- **DALL-E**: A model for generating images from text descriptions.

### CLI (Command Line Interface) 💻
- OpenAI offers command-line interface support, making it easier to automate tasks.

### File Upload with Azure Storage Account 📂
- Use **Azure Blob Storage** to upload and process large volumes of data, such as text files or other content that needs to be analyzed by the model.

## System Message 🛠️

The **System Message** is a special type of message that defines the model's behavior in a conversation. It can be used to guide how the model responds.

### Types of Responses:
- **Zero-shot**: The model responds without prior training or preparation on the subject.
- **Direct response**: The model answers directly to the prompt, without relying on additional context.
- **Based on the prompt only**: The model uses only the information provided in the prompt.

## How Response Formulation Works 🧑‍💻

Model responses are formulated considering:
- **Max Response**: The model can generate a complete response up to the defined token limit.
- **Previous Messages**: When using multiple interactions, previous messages may be included to provide context and improve response coherence.

## Temperature vs. Top-P ⚖️

These two parameters help control the creativity and diversity of the responses.

### Temperature:
- **Temperature 0**: More deterministic, predictable, and direct responses.
- **Temperature 1**: More random, creative, and varied responses.

### Top-P:
- Controls the cumulative probability of chosen words.
- **Top-P from 0.1 to 0.9**: The model selects words whose cumulative probability reaches the *p* value.

**Tip:** Use **Top P** or **Temperature**, rarely both, as both affect the level of randomness.

## Frequency Penalty vs. Presence Penalty 🔁

- **Frequency Penalty**: Penalizes the repetition of frequently used words.
- **Presence Penalty**: Penalizes the repetition of words that have already appeared, helping to increase response diversity.

## How to Create Good Images Using DALL-E 🖼️

When using the **DALL-E** model to generate images, keep the following tips in mind:

### Tips for good images:
- **Clarity**: Be clear and direct in describing what you want in the image.
- **Specificity**: The more details, the better the image quality.
- **Context**: Include any necessary context to bring your description to life.
- **Structure**: Organize your ideas logically and coherently to make image creation easier.

---

I hope this guide helps you understand the features and how to use them effectively! 🚀

---

PT-BR
# Azure Open AI - Funcionalidades

Este repositório contém informações sobre as principais funcionalidades do Azure Open AI, incluindo LLMs, modelos, tokenização, e mais.

## LLMs (Large Language Models) 💡

Os **LLMs** (Large Language Models) são modelos de aprendizado profundo treinados com grandes volumes de texto para gerar, entender e processar linguagem humana. 

LLMs são a peça chave por trás da geração de texto. Em resumo, eles consistem em grandes modelos transformer pré-treinados, treinados para prever a próxima palavra (ou, mais precisamente, o próximo token) com base em um texto de entrada. Como eles predizem um token por vez, é necessário realizar um processo mais elaborado para gerar novas frases, em vez de apenas chamar o modelo — é necessário usar a geração autorregressiva.

- **O que são?** São redes neurais que podem realizar uma ampla gama de tarefas, como tradução, geração de texto, resumo, etc.
- **Em poucas palavras:** Eles podem "aprender" a partir de grandes conjuntos de dados e aplicar esse conhecimento a uma infinidade de tarefas linguísticas.

Saiba mais: [LLM Tutorial na Hugging Face](https://huggingface.co/docs/transformers/llm_tutorial)

## Tokenização da Open AI 🔑

A **tokenização** é o processo de dividir texto em unidades menores chamadas *tokens*. Estes tokens podem ser palavras, partes de palavras ou até mesmo caracteres individuais. A OpenAI usa tokenização para entender e processar o texto de maneira eficiente.

## Playground 🛠️

O **Playground** da OpenAI oferece uma interface interativa para testar modelos de linguagem com diversos parâmetros. Algumas das principais opções são:

### Temperatura 🌡️
- **O que é?** Controla a aleatoriedade nas respostas geradas. 
  - **Temperatura 0**: Respostas mais determinísticas.
  - **Temperatura 1**: Respostas mais criativas e variadas.

### Top P 🎯
- **O que é?** Um método alternativo ao controle de temperatura, usando uma abordagem probabilística para escolher as palavras.
  - **Top P de 0.1 a 0.9**: A probabilidade acumulada de palavras escolhidas pelo modelo.

### Tokens Máximos 🧑‍💻
- **O que é?** Limita o número de tokens gerados em uma resposta.

### Penalidades ⚖️
- **Penalidade de Frequência**: Reduz a repetição excessiva de palavras.
- **Penalidade de Presença**: Penaliza a repetição de termos já usados, aumentando a diversidade da resposta.

### Sistema de Mensagens 💬
- **O que é?** Permite interagir com o modelo em uma sequência de mensagens. Útil para criar conversas ou prompts mais contextuais.
  
### Engenharia de Prompt 📝
- **O que é?** A arte de estruturar os prompts de forma que o modelo entenda melhor o que é solicitado.

## Modelos Open AI 🧠

A OpenAI oferece diversos modelos para diferentes finalidades:

- **GPT-3 (gpt-3.5, gpt-3.5-turbo)**: Modelos de linguagem geral.
- **GPT-4**: A versão mais avançada, com maior capacidade de compreensão e geração.
- **GPT-1 Mini**: Uma versão compacta e otimizada do GPT-1.
- **GPT-4 Turbo**: Versão otimizada do GPT-4, com maior velocidade e custos reduzidos.
- **DALL-E**: Modelo para geração de imagens a partir de descrições de texto.

### CLI (Interface de Linha de Comando) 💻
- A OpenAI oferece suporte para interação através de linha de comando, facilitando a automação de tarefas.

### Upload de Arquivos com Azure Storage Account 📂
- Use **Blob Storage** do Azure para carregar e processar grandes volumes de dados, como arquivos de texto ou outros conteúdos que precisam ser analisados pelo modelo.

## System Message 🛠️

O **System Message** é um tipo especial de mensagem que define o comportamento do modelo em uma conversa. Ele pode ser usado para guiar como o modelo responde.

### Tipos de Respostas:
- **Zero-shot**: O modelo responde sem ter sido treinado ou preparado previamente sobre o assunto.
- **Resposta direta**: O modelo responde diretamente ao prompt, sem depender de contexto adicional.
- **Baseada apenas no prompt**: O modelo utiliza apenas a informação fornecida no prompt.

## Como funciona a Formulação de Respostas 🧑‍💻

As respostas do modelo são formadas levando em consideração:
- **Resposta Máxima**: O modelo pode gerar uma resposta completa até o limite de tokens definidos.
- **Mensagens Anteriores**: Quando se utiliza múltiplas interações, as mensagens anteriores podem ser incluídas para fornecer contexto e melhorar a coerência das respostas.

## Temperatura vs. Top-P ⚖️

Esses dois parâmetros ajudam a controlar a criatividade e a diversidade das respostas.

### Temperatura:
- **Temperatura 0**: Mais determinista, respostas mais previsíveis e diretas.
- **Temperatura 1**: Mais aleatória, respostas mais criativas e variadas.

### Top-P:
- Controla a probabilidade cumulativa de palavras sendo escolhidas.
- **Top-P de 0.1 a 0.9**: O modelo escolhe palavras com uma probabilidade acumulada que atinge o valor de *p*.

**Dica:** Use **Top P** ou **Temperatura**, raramente ambos, pois ambos afetam o nível de aleatoriedade.

## Frequency Penalty vs. Presence Penalty 🔁

- **Frequency Penalty**: Penaliza a repetição de palavras frequentemente usadas.
- **Presence Penalty**: Penaliza a repetição de palavras já mencionadas, ajudando a aumentar a diversidade das respostas.

## Como Criar Boas Imagens com o DALL-E 🖼️

Quando utilizar o modelo **DALL-E** para gerar imagens, tenha em mente as seguintes dicas:

### Dicas para boas imagens:
- **Clareza**: Seja claro e direto ao descrever o que deseja na imagem.
- **Especificidade**: Quanto mais detalhes, melhor será a qualidade da imagem gerada.
- **Contexto**: Inclua o contexto necessário para dar vida à sua descrição.
- **Estrutura**: Organize suas ideias de forma lógica e coerente para facilitar a criação da imagem.

---

Espero que esse guia ajude a entender as funcionalidades e como usá-las de forma eficaz! 🚀
