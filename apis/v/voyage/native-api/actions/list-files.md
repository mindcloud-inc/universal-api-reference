# List Files with Voyage

Retrieves files from Voyage.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/files`
- **Base URL:** `https://api.voyageai.com`
- **Official documentation:** [List Files](https://docs.voyageai.com/reference/list-files)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `purpose` | query | `string` | no | Filter files by purpose. |
| `order` | query | `list` | no | Sort order for files by creation time. Accepted values: `0`, `1`. |
