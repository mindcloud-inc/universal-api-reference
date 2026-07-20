# Update Channel with Callbell

Updates an existing channel in Callbell.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/channels/:uuid`
- **Base URL:** `https://api.callbell.eu/v1`
- **Official documentation:** [Update Channel](https://docs.callbell.eu/api/reference/channels_api/patch_channel/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | no | New title for the channel. |
| `uuid` | path | `string` | yes | Unique identifier of the channel to update. |
