# Subscribe To Notifications with Chatforma

Creates a new notification subscription in Chatforma.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribe-notification`
- **Base URL:** `https://api.pro.chatforma.com/public/v1`
- **Official documentation:** [Subscribe To Notifications](https://docs.chatforma.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | body | `number` | yes | Bot ID to subscribe notifications for |
| `formId` | body | `string` | yes | Form ID to subscribe notifications for |
| `target_url` | body | `string` | yes | Webhook URL that should receive notifications |
| `event` | body | `string` | no | Optional event to subscribe to |
