# Delete Message with Discord

Deletes a message from a Discord channel.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/channels/:channelId/messages/:messageId`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Delete Message](https://docs.discord.com/developers/resources/message#delete-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | Channel identifier. |
| `messageId` | path | `string` | yes | Message identifier. |
