# Send Direct Message to Group with Pumble

Creates a direct message to a Pumble user group.

## Endpoint

- **Method:** `POST`
- **Path:** `/dmGroup`
- **Base URL:** `https://pumble-api-keys.addons.marketplace.cake.com`
- **Official documentation:** [Send Direct Message to Group](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | no | Array of email addresses to include in the group DM. |
| `text` | body | `string` | yes | — |
| `userIds[]` | body | `array<string>` | no | Array of user IDs to include in the group DM. |
