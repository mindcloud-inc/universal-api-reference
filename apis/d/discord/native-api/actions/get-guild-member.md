# Get Guild Member with Discord

Retrieves a Discord guild member by user ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/guilds/:guildId/members/:userId`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Get Guild Member](https://docs.discord.com/developers/resources/guild#get-guild-member)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guildId` | path | `string` | yes | ID of the guild. |
| `userId` | path | `string` | yes | ID of the user/member. |
