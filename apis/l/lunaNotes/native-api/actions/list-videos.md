# List Videos with LunaNotes

Retrieves videos from LunaNotes.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/videos`
- **Base URL:** `https://api.lunanotes.io`
- **Official documentation:** [List Videos](https://lunanotes.io/docs/videos/get-v1-videos)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | query | `string` | no | Filter by YouTube channel ID. |
| `folderId` | query | `string` | no | Filter by folder ID. Use null for root videos. |
| `include` | query | `string` | no | Comma-separated list of related resources to include. |
| `v` | query | `string` | no | Filter by YouTube video ID. |
