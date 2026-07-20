# List Chat Messages with Smart Sender

Retrieves messages for a chat in Smart Sender.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/chats/:chatId/messages`
- **Base URL:** `https://api.smartsender.com`
- **Official documentation:** [List Chat Messages](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676575830/Messages%2BAPI%2B-%2Ben)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activities` | query | `boolean` | no | Whether to include system messages in the results. |
| `chatId` | path | `string` | yes | The Smart Sender chat ID. |
