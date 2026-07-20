# Search Guild Members with Discord-Bot

Finds Discord guild members by username or nickname prefix.

## Endpoint

- **Method:** `GET`
- **Path:** `/guilds/:guildId/members/search`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Search Guild Members](https://docs.discord.com/developers/resources/guild#search-guild-members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guildId` | path | `string` | yes | Discord guild (server) ID. |
| `query` | query | `string` | yes | Username or nickname prefix to search for. |
