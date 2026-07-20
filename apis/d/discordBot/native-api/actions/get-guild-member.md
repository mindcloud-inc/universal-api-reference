# Get Guild Member with Discord-Bot

Retrieves a member from a Discord guild.

## Endpoint

- **Method:** `GET`
- **Path:** `/guilds/:guildId/members/:userId`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Get Guild Member](https://docs.discord.com/developers/resources/guild#get-guild-member)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guildId` | path | `string` | yes | Discord guild (server) ID. |
| `userId` | path | `string` | yes | Discord user ID. |
