# List Guild Members with Discord

Lists members in a Discord guild.

## Endpoint

- **Method:** `GET`
- **Path:** `/guilds/:guildId/members`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [List Guild Members](https://docs.discord.com/developers/resources/guild#list-guild-members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guildId` | path | `string` | yes | ID of the guild. |
| `limit` | query | `number` | no | Max members to return (1-1000). |
| `after` | query | `string` | no | Return members after this user ID. |
