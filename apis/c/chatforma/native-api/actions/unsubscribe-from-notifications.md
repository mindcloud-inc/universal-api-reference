# Unsubscribe From Notifications with Chatforma

Deletes a notification subscription from Chatforma.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/unsubscribe-notification`
- **Base URL:** `https://api.pro.chatforma.com/public/v1`
- **Official documentation:** [Unsubscribe From Notifications](https://docs.chatforma.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | body | `number` | yes | Bot ID that owns the notification subscription |
| `subscriptionId` | body | `number` | yes | Notification subscription ID to delete |
