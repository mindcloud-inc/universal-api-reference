# List Guild Channels with Discord-Bot

Retrieves channels for a Discord guild.

## Endpoint

- **Method:** `GET`
- **Path:** `/guilds/:guildId/channels`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [List Guild Channels](https://docs.discord.com/developers/resources/guild#get-guild-channels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guildId` | path | `string` | yes | Discord guild (server) ID. |
