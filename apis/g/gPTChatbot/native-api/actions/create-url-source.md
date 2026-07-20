# Create URL Source with GPT Chatbot

Creates a URL source for a chatbot in GPT Chatbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/chatbot/:uuid/data-source/url`
- **Base URL:** `https://app.gptchatbot.it/api/v1`
- **Official documentation:** [Create URL Source](https://docs.gptchatbot.it/api-reference/data-sources/create-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Source URL. |
| `uuid` | path | `string` | yes | Chatbot uuid. |
