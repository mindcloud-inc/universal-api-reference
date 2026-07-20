# List Comments with YouTube

Retrieves comments or replies from YouTube.

## Endpoint

- **Method:** `GET`
- **Path:** `/youtube/v3/comments`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [List Comments](https://developers.google.com/youtube/v3/docs/comments/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `part` | query | `string` | yes | Comma-separated comment resource parts to include. |
| `parentId` | query | `string` | no | Retrieve replies for a top-level comment ID. |
| `id` | query | `string` | no | Comma-separated list of comment IDs. |
| `textFormat` | query | `string` | no | Comment text format, html or plainText. |
