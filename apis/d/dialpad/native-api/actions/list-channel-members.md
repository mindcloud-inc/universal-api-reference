# List Channel Members with Dialpad

Retrieves members of a Dialpad channel.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/:id/members`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [List Channel Members](https://developers.dialpad.com/reference/channelsmemberslist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The channel id. |
| `cursor` | query | `string` | no | A token used to return the next page of a previous request. Use the cursor provided in the previous response. |
