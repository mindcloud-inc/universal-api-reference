# List Current User Guilds with Discord

Lists the current user's guilds in Discord.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/@me/guilds`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [List Current User Guilds](https://docs.discord.com/developers/resources/user#get-current-user-guilds)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of guilds to return (1-200). |
| `with_counts` | query | `boolean` | no | Include approximate member and presence counts. |
| `before` | query | `string` | no | Get guilds before this guild ID. |
| `after` | query | `string` | no | Get guilds after this guild ID. |
