# List Channels with Dialpad

Retrieves company channel records from Dialpad.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [List Channels](https://developers.dialpad.com/reference/channelslist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `state` | query | `string` | no | The state of the channel. |
| `cursor` | query | `string` | no | A token used to return the next page of a previous request. Use the cursor provided in the previous response. |
