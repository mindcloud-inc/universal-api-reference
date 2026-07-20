# List Channels with Callbell

Retrieves channels for the current Callbell account.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels`
- **Base URL:** `https://api.callbell.eu/v1`
- **Official documentation:** [List Channels](https://docs.callbell.eu/api/reference/channels_api/get_channels/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | query | `boolean` | no | Filter channels by active state. |
| `page` | query | `number` | no | Page number to retrieve. |
| `type` | query | `string` | no | Filter channels by type. |
