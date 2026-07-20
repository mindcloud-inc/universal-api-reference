# Query Chatbot with DenserChat

Retrieves a chatbot answer from DenserChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/query`
- **Base URL:** `https://denser.ai/api`
- **Official documentation:** [Query Chatbot](https://docs.denser.ai/docs/api/chat/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `question` | body | `string` | yes | The question to send to the Denser chatbot. |
| `context[]` | body | `array<object>` | no | Prior conversation turns to send with the question. |
| `prompt` | body | `string` | no | An optional prompt override for this request. |
| `model` | body | `list<string>` | no | An optional model name for this request. Accepted values: `claude-3-5-haiku`, `claude-3-5-sonnet`, `claude-3-7-sonnet`, `gpt-3.5`, `gpt-4`, `gpt-4o`, `gpt-4o-mini`. |
| `citation` | body | `boolean` | no | Whether to include citations in the response. |
