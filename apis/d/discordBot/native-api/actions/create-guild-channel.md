# Create Guild Channel with Discord-Bot

Creates a channel in a Discord guild.

## Endpoint

- **Method:** `POST`
- **Path:** `/guilds/:guildId/channels`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Create Guild Channel](https://docs.discord.com/developers/resources/guild#create-guild-channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guildId` | path | `string` | yes | Discord guild (server) ID. |
| `name` | body | `string` | yes | Channel name. |
