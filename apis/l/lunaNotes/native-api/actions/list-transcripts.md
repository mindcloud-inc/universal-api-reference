# List Transcripts with LunaNotes

Retrieves transcripts from LunaNotes.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/transcripts`
- **Base URL:** `https://api.lunanotes.io`
- **Official documentation:** [List Transcripts](https://lunanotes.io/docs/transcripts/get-v1-transcripts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include` | query | `string` | no | Comma-separated list of related resources to include. |
| `kind` | query | `string` | no | Filter by transcript type or source. |
| `language` | query | `string` | no | Filter by language code such as en or es. |
| `videoId` | query | `string` | no | Filter by video ID. |
