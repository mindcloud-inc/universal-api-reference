# List Scores with Langfuse

Retrieves scores from Langfuse.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/scores`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [List Scores](https://api.reference.langfuse.com/#tag/Scores/GET/api/public/v2/scores)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `configId` | query | `string` | no |
| `datasetRunId` | query | `string` | no |
| `dataType` | query | `string` | no |
| `environment` | query | `string` | no |
| `fields` | query | `string` | no |
| `filter` | query | `string` | no |
| `fromTimestamp` | query | `string` | no |
| `name` | query | `string` | no |
| `observationId` | query | `string` | no |
| `operator` | query | `string` | no |
| `queueId` | query | `string` | no |
| `scoreIds` | query | `string` | no |
| `sessionId` | query | `string` | no |
| `source` | query | `string` | no |
| `toTimestamp` | query | `string` | no |
| `traceId` | query | `string` | no |
| `traceTags` | query | `string` | no |
| `userId` | query | `string` | no |
| `value` | query | `string` | no |
