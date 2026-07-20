# List Guild Roles with Discord-Bot

Retrieves roles from a Discord guild.

## Endpoint

- **Method:** `GET`
- **Path:** `/guilds/:guildId/roles`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [List Guild Roles](https://docs.discord.com/developers/resources/guild#get-guild-roles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guildId` | path | `string` | yes | Discord guild (server) ID. |
