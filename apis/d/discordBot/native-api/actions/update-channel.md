# Update Channel with Discord-Bot

Updates an existing channel in Discord.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/channels/:channelId`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Update Channel](https://docs.discord.com/developers/resources/channel#modify-channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | Discord channel ID. |
| `name` | body | `string` | no | New channel name. |
