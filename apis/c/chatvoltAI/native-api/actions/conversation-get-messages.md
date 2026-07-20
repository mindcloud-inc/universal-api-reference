# Get Messages with Chatvolt AI

Retrieves messages from Chatvolt AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversation/{conversationId}/messages/{count}`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Get Messages](https://docs.chatvolt.ai/api-reference/endpoint/conversation/get-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | yes | ID of the conversation from which the messages will be retrieved. |
| `count` | path | `number` | yes | Number of most recent messages to be retrieved. If not specified, the default is 2. |
