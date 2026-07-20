# Delete Source with GPT Chatbot

Deletes an existing source from GPT Chatbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/data-source/:uuid/delete`
- **Base URL:** `https://app.gptchatbot.it/api/v1`
- **Official documentation:** [Delete Source](https://docs.gptchatbot.it/api-reference/data-sources/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Source uuid. |
