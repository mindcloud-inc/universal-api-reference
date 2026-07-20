# Remove Guild Ban with Discord

Removes a guild ban in Discord.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/guilds/:guildId/bans/:userId`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Remove Guild Ban](https://docs.discord.com/developers/resources/guild#remove-guild-ban)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guildId` | path | `string` | yes | Target guild ID |
| `userId` | path | `string` | yes | User ID to unban |
