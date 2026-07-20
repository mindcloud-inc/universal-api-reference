# Update Source with GPT Chatbot

Updates an existing source in GPT Chatbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/data-source/:uuid/update`
- **Base URL:** `https://app.gptchatbot.it/api/v1`
- **Official documentation:** [Update Source](https://docs.gptchatbot.it/api-reference/data-sources/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Source title. |
| `uuid` | path | `string` | yes | Source uuid. |
