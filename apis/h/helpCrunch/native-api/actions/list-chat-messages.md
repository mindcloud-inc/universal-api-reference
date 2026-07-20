# List Chat Messages with HelpCrunch

Retrieves messages from a chat in HelpCrunch.

## Endpoint

- **Method:** `GET`
- **Path:** `/chats/:chatId/messages`
- **Base URL:** `https://api.helpcrunch.com/v1`
- **Official documentation:** [List Chat Messages](https://docs.helpcrunch.com/en/rest-api-v1/get-messages-v1)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chatId` | path | `number` | yes |
