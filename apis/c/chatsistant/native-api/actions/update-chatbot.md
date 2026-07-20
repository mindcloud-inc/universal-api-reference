# Update Chatbot with Chatsistant

Updates an existing chatbot in Chatsistant.

## Endpoint

- **Method:** `POST`
- **Path:** `/chatbot/:uuid/update`
- **Base URL:** `https://app.chatsistant.com/api/v1`
- **Official documentation:** [Update Chatbot](https://docs.chatsistant.com/api-reference/chatbots/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | no | The model name. |
| `name` | body | `string` | no | The chatbot name. |
| `prompt` | body | `string` | no | The chatbot prompt. |
| `temperature` | body | `string` | no | The chatbot temperature. |
| `uuid` | path | `string` | no | The chatbot UUID. |
| `visibility` | body | `string` | no | The chatbot visibility. |
