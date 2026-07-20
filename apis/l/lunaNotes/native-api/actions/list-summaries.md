# List Summaries with LunaNotes

Retrieves summaries from LunaNotes.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/summaries`
- **Base URL:** `https://api.lunanotes.io`
- **Official documentation:** [List Summaries](https://lunanotes.io/docs/summaries/get-v1-summaries)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `flagged` | query | `boolean` | no | Filter by moderation status. |
| `include` | query | `string` | no | Comma-separated list of related resources to include. |
| `slug` | query | `string` | no | Filter by slug using an exact match. |
| `transcriptId` | query | `string` | no | Filter by transcript ID. |
| `videoId` | query | `string` | no | Filter by video ID. |
