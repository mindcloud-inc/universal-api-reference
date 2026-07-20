# Get available libraries for the team with Digital Samba

Retrieves team libraries from Digital Samba.

## Endpoint

- **Method:** `GET`
- **Path:** `/libraries`
- **Base URL:** `https://api.digitalsamba.com/api/v1`
- **Official documentation:** [Get available libraries for the team](https://developer.digitalsamba.com/rest-api/#libraries-GETapi-v1-libraries)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | The UUID of the library after which records will be returned. |
