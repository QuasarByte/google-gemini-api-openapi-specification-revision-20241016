# Google Generative Language API OpenAPI Specification (Revision 20241016)

This repository contains the OpenAPI 3.0.0 specification for the **Google Generative Language API**, which allows developers to generate a **Google Generative Language Client Library** using tools like OpenAPI Generator.

## Overview of the Generative Language API

The **Generative Language API** enables developers to create AI applications powered by the **Gemini** model, a cutting-edge multimodal large language model (LLM). **Gemini** can understand and generate content across various media types, including text, images, audio, and video.

### Use Cases:
- **Reasoning and Comprehension**: Gemini supports complex reasoning across multimodal inputs.
- **Content Generation**: Create rich, varied content such as dialogue systems, stories, or other creative outputs.
- **Summarization and Classification**: Generate summaries, perform text classification, and more using the model’s powerful capabilities.

## Key Features

- **Multimodal Support**: The ability to work with text, images, audio, and video data for generating or reasoning with content.
- **Generative Capabilities**: Build applications for content generation, dialogue agents, or classification tasks.
- **Advanced Safety Mechanisms**: Provides safety settings to prevent harmful or inappropriate content generation.

## Tested Endpoints

The only endpoint thoroughly tested so far is:
- `/v1beta/models/{model}:generateContent`: This endpoint generates content based on the input provided.

## How to Generate the Client Library

You can generate a client library using the **[`openapi-generator-cli`](https://openapi-generator.tech/docs/installation/#jar)** tool. The OpenAPI Generator supports multiple programming languages and allows for easy client library generation.

### Example: Generating the Client Library for Java

Below is an example command for generating a Java client library using the **`openapi-generator-cli`** tool:

#### Windows Shell Command

```shell
java -jar openapi-generator-cli-7.9.0.jar ^
generate -g java ^
-i generativelanguage-openapi-20241016.json ^
-o ./generated-client-java ^
--group-id com.example ^
--artifact-id google-generativelanguage ^
--api-package com.example.google.generativelanguage ^
--model-package com.example.google.generativelanguage.domain ^
--import-mappings=DateTime=java.time.LocalDateTime ^
--type-mappings=DateTime=java.time.LocalDateTime ^
--additional-properties=library=native,openApiNullable=false,invokerPackage=com.example.google.generativelanguage.client
