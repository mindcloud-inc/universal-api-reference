# Delete Guild Role with Discord-Bot

Deletes a role from a Discord guild.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/guilds/:guildId/roles/:roleId`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Delete Guild Role](https://docs.discord.com/developers/resources/guild#delete-guild-role)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guildId` | path | `string` | yes | Discord guild (server) ID. |
| `roleId` | path | `string` | yes | Discord role ID. |
