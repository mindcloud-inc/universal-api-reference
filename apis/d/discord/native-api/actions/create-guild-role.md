# Create Guild Role with Discord

Creates a new role in a Discord guild.

## Endpoint

- **Method:** `POST`
- **Path:** `/guilds/:guildId/roles`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Create Guild Role](https://docs.discord.com/developers/resources/guild#create-guild-role)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guildId` | path | `string` | yes | Target guild ID |
| `name` | body | `string` | no | Role name (max 100 chars) |
| `permissions` | body | `string` | no | Bitwise permissions string |
| `colors` | body | `object` | no | Role colors object |
| `color` | body | `number` | no | Deprecated RGB color integer |
| `hoist` | body | `boolean` | no | Display role separately |
| `icon` | body | `string` | no | Role icon image data |
| `unicode_emoji` | body | `string` | no | Role unicode emoji |
| `mentionable` | body | `boolean` | no | Whether role is mentionable |
