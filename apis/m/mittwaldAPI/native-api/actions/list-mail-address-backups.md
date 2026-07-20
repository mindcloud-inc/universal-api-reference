# List Mail Address Backups with mittwald

Retrieves mail address backups from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/mail-addresses/:mailAddressId/backups`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [List Mail Address Backups](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mailAddressId` | path | `string` | yes | The unique identifier of the mail address. |
