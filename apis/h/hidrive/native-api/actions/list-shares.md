# List Shares with HiDrive

Retrieves shares from HiDrive.

## Endpoint

- **Method:** `GET`
- **Path:** `/share`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [List Shares](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/share_GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Comma-separated share fields to include. |
| `id` | query | `string` | no | Share ID to retrieve. |
| `path` | query | `string` | no | Shared path. |
| `pid` | query | `string` | no | Shared path public ID. |
