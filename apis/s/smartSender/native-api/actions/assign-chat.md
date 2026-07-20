# Assign Chat with Smart Sender

Assigns a chat to an operator in Smart Sender.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/chats/:chatId/forward/:operatorId`
- **Base URL:** `https://api.smartsender.com`
- **Official documentation:** [Assign Chat](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676542648/Chats%2BAPI%2B-%2Ben)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | The Smart Sender chat ID. |
| `operatorId` | path | `string` | yes | The Smart Sender operator ID that should receive the chat. |
