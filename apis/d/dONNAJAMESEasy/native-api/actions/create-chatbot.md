# Create Chatbot with DONNAJAMES Easy

Creates a new chatbot in DONNAJAMES Easy.

## Endpoint

- **Method:** `POST`
- **Path:** `chatbot/create`
- **Base URL:** `https://app.gpt-trainer.com/api/v1`
- **Official documentation:** [Create Chatbot](https://guide.gpt-trainer.com/api-reference/chatbots/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `visibility` | body | `string` | no |
| `rate_limit[]` | body | `array<number>` | no |
| `rate_limit_message` | body | `string` | no |
| `show_citations` | body | `boolean` | no |
