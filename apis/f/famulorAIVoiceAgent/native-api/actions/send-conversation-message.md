# Send Conversation Message with Famulor AI - Voice Agent

Sends a message to a Famulor conversation and returns the reply.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/:uuid/messages`
- **Base URL:** `https://app.famulor.de/api`
- **Official documentation:** [Send Conversation Message](https://docs.famulor.io/en/api-reference/ai-chatbot/send-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | Message text to send into the conversation. |
| `uuid` | path | `string` | yes | Conversation UUID. |
