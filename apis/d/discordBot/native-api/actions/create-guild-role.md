# Create Guild Role with Discord-Bot

Creates a role in a Discord guild.

## Endpoint

- **Method:** `POST`
- **Path:** `/guilds/:guildId/roles`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Create Guild Role](https://docs.discord.com/developers/resources/guild#create-guild-role)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guildId` | path | `string` | yes | Discord guild (server) ID. |
| `name` | body | `string` | no | Role name. |
