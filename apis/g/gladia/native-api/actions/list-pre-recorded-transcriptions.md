# List Pre-recorded Transcriptions with Gladia

Retrieves pre-recorded transcription jobs from Gladia.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/pre-recorded`
- **Base URL:** `https://api.gladia.io`
- **Official documentation:** [List Pre-recorded Transcriptions](https://docs.gladia.io/api-reference/v2/pre-recorded/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `date` | no | Filter items relevant to a specific date in ISO format (YYYY-MM-DD). |
| `before_date` | query | `date` | no | Include items that occurred before the specified date in ISO format. |
| `after_date` | query | `date` | no | Filter for items after the specified date. Use with before_date for a range. |
| `status` | query | `list<string>` | no | Filter the list based on item status. Accepted values: `done`, `error`, `processing`, `queued`. |
