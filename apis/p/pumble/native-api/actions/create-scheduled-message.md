# Create Scheduled Message with Pumble

Creates a scheduled message in Pumble.

## Endpoint

- **Method:** `POST`
- **Path:** `/createScheduledMessage`
- **Base URL:** `https://pumble-api-keys.addons.marketplace.cake.com`
- **Official documentation:** [Create Scheduled Message](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | body | `string` | no | — |
| `sendAt` | body | `number` | no | Unix timestamp in milliseconds for when the message should be sent. |
| `text` | body | `string` | no | — |
