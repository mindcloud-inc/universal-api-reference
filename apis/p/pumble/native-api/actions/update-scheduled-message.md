# Update Scheduled Message with Pumble

Updates an existing scheduled message in Pumble.

## Endpoint

- **Method:** `POST`
- **Path:** `/editScheduledMessage`
- **Base URL:** `https://pumble-api-keys.addons.marketplace.cake.com`
- **Official documentation:** [Update Scheduled Message](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | body | `string` | no | — |
| `scheduledMessageId` | body | `string` | no | — |
| `sendAt` | body | `number` | no | Unix timestamp in milliseconds for the updated scheduled send time. |
| `text` | body | `string` | no | — |
