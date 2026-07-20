# Update Chatbot with DONNAJAMES Easy

Updates an existing chatbot in DONNAJAMES Easy.

## Endpoint

- **Method:** `POST`
- **Path:** `chatbot/:uuid/update`
- **Base URL:** `https://app.gpt-trainer.com/api/v1`
- **Official documentation:** [Update Chatbot](https://guide.gpt-trainer.com/api-reference/chatbots/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | — |
| `rate_limit_message` | body | `string` | no | — |
| `uuid` | path | `string` | yes | Chatbot uuid |
| `visibility` | body | `string` | no | — |
| `show_citations` | body | `boolean` | no | — |
