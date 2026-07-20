# List Transcriptions with GetTranscribe

Retrieves transcriptions from GetTranscribe by filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/transcriptions`
- **Base URL:** `https://api.gettranscribe.ai`
- **Official documentation:** [List Transcriptions](https://www.gettranscribe.ai/api-documentation/transcriptions/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_id` | query | `number` | no | Filter transcriptions by folder ID. |
| `platform` | query | `string` | no | Filter transcriptions by source platform. Accepted values: `0`, `1`, `2`. |
