# Add Users to Channel with Pumble

Adds users to a Pumble channel.

## Endpoint

- **Method:** `POST`
- **Path:** `/addUsersToChannel`
- **Base URL:** `https://pumble-api-keys.addons.marketplace.cake.com`
- **Official documentation:** [Add Users to Channel](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | body | `string` | no | — |
| `userIds[]` | body | `array<string>` | no | Array of user IDs to add to the channel. |
