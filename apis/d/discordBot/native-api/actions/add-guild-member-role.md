# Add Guild Member Role with Discord-Bot

Adds a role to a Discord guild member.

## Endpoint

- **Method:** `PUT`
- **Path:** `/guilds/:guildId/members/:userId/roles/:roleId`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Add Guild Member Role](https://docs.discord.com/developers/resources/guild#add-guild-member-role)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guildId` | path | `string` | yes | Discord guild (server) ID. |
| `userId` | path | `string` | yes | Discord user ID. |
| `roleId` | path | `string` | yes | Discord role ID. |
