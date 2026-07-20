# Create Guild Ban with Discord

Creates a guild ban in Discord.

## Endpoint

- **Method:** `PUT`
- **Path:** `/guilds/:guildId/bans/:userId`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Create Guild Ban](https://docs.discord.com/developers/resources/guild#create-guild-ban)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guildId` | path | `string` | yes | Target guild ID |
| `userId` | path | `string` | yes | User ID to ban |
| `delete_message_seconds` | body | `number` | no | Delete message history in seconds (0-604800) |
| `delete_message_days` | body | `number` | no | Deprecated delete window in days (0-7) |
