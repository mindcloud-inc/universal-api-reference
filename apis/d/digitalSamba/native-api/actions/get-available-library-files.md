# Get available library files with Digital Samba

Retrieves library files from Digital Samba.

## Endpoint

- **Method:** `GET`
- **Path:** `/libraries/:library/files`
- **Base URL:** `https://api.digitalsamba.com/api/v1`
- **Official documentation:** [Get available library files](https://developer.digitalsamba.com/rest-api/#libraries-GETapi-v1-libraries--library--files)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `library` | path | `string` | yes | Library path parameter. |
| `after` | query | `string` | no | The UUID of the file after which records will be returned. |
