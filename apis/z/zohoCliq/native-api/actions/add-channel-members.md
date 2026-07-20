# Add Channel Members with Zoho Cliq

Adds members to a Zoho Cliq channel.

## Endpoint

- **Method:** `POST`
- **Path:** `/channels/:channelId/members`
- **Base URL:** `https://cliq.zoho.com/api/v2`
- **Official documentation:** [Add Channel Members](https://www.zoho.com/cliq/help/restapi/v2/#Channels_Add_Members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | The ID of the channel where members should be added. |
| `user_ids[]` | body | `array<string>` | yes | The user IDs to add to the channel. |
