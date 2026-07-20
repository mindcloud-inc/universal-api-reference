# Remove Guild Member with Discord

Removes a member from a Discord guild.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/guilds/:guildId/members/:userId`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Remove Guild Member](https://docs.discord.com/developers/resources/guild#remove-guild-member)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guildId` | path | `string` | yes | ID of the guild. |
| `userId` | path | `string` | yes | ID of the user/member to remove. |
