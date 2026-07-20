# List Notifications with Chatforma

Retrieves notification subscription records from Chatforma.

## Endpoint

- **Method:** `GET`
- **Path:** `/notification`
- **Base URL:** `https://api.pro.chatforma.com/public/v1`
- **Official documentation:** [List Notifications](https://docs.chatforma.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | query | `number` | yes | Bot ID to list notification subscriptions for |
| `formId` | query | `string` | yes | Form ID to filter notification subscriptions by |
