# Get one Message with Chatvolt AI

Retrieves a message from Chatvolt AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages/{messageId}`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Get one Message](https://docs.chatvolt.ai/api-reference/endpoint/conversation/get-one-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | Message ID. |
| `includeSources` | query | `boolean` | no | Include the 'sources' property in the response. |
