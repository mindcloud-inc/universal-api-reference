# List Channel Members with Zoho Cliq

Retrieves members of a Zoho Cliq channel.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/:channelId/members`
- **Base URL:** `https://cliq.zoho.com/api/v2`
- **Official documentation:** [List Channel Members](https://www.zoho.com/cliq/help/restapi/v2/#Channels_Get_Members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | The ID of the channel whose members should be retrieved. |
