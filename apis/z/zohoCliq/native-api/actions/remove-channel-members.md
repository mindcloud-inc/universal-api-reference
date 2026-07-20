# Remove Channel Members with Zoho Cliq

Removes members from a Zoho Cliq channel.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/channels/:channelId/members`
- **Base URL:** `https://cliq.zoho.com/api/v2`
- **Official documentation:** [Remove Channel Members](https://www.zoho.com/cliq/help/restapi/v2/#Channels_Delete_Members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | The ID of the channel where members should be removed. |
| `user_ids[]` | body | `array<string>` | yes | The user IDs to remove from the channel. |
| `silent` | body | `boolean` | no | When true, remove members without sending notifications. |
