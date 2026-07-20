# Create QA Source with GPT Chatbot

Creates a QA source for a chatbot in GPT Chatbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/chatbot/:uuid/data-source/qa`
- **Base URL:** `https://app.gptchatbot.it/api/v1`
- **Official documentation:** [Create QA Source](https://docs.gptchatbot.it/api-reference/data-sources/create-qa)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `answer` | body | `string` | yes | Answer text. |
| `question` | body | `string` | yes | Question text. |
| `uuid` | path | `string` | yes | Chatbot uuid. |
