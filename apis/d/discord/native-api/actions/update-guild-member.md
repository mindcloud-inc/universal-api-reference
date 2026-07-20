# Update Guild Member with Discord

Updates a member in a Discord guild.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/guilds/:guildId/members/:userId`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Update Guild Member](https://docs.discord.com/developers/resources/guild#modify-guild-member)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guildId` | path | `string` | yes | ID of the guild. |
| `userId` | path | `string` | yes | ID of the user/member to modify. |
| `nick` | body | `string` | no | Value to set users nickname to. |
| `roles[]` | body | `array<string>` | no | Array of role IDs assigned to the member. |
| `mute` | body | `boolean` | no | Whether the user is muted in voice channels. |
| `deaf` | body | `boolean` | no | Whether the user is deafened in voice channels. |
| `channel_id` | body | `string` | no | ID of voice channel to move user to (or null). |
| `communication_disabled_until` | body | `date` | no | ISO8601 timestamp for timeout expiration (or null). |
