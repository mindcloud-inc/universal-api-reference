# List Transcripts with AssemblyAI

Retrieves transcript records from your AssemblyAI account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/transcript`
- **Base URL:** `https://api.assemblyai.com`
- **Official documentation:** [List Transcripts](https://www.assemblyai.com/docs/api-reference/transcripts/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of transcripts to retrieve. |
| `status` | query | `string` | no | Filter transcripts by status. |
| `created_on` | query | `date` | no | Only return transcripts created on this date. |
| `before_id` | query | `string` | no | Return transcripts created before this transcript ID. |
| `after_id` | query | `string` | no | Return transcripts created after this transcript ID. |
| `throttled_only` | query | `boolean` | no | Only return throttled transcripts. |
