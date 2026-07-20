# List Guild Members with Discord-Bot

Retrieves members from a Discord guild.

## Endpoint

- **Method:** `GET`
- **Path:** `/guilds/:guildId/members`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [List Guild Members](https://docs.discord.com/developers/resources/guild#list-guild-members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Return members after this user ID. Discord defaults to 0 when omitted. |
| `guildId` | path | `string` | yes | Discord guild (server) ID. |
