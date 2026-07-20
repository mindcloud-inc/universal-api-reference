# List Observations with Langfuse

Retrieves observations from Langfuse.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/observations`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [List Observations](https://api.reference.langfuse.com/#tag/Observations/GET/api/public/v2/observations)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cursor` | query | `string` | no |
| `environment` | query | `string` | no |
| `expandMetadata` | query | `string` | no |
| `fields` | query | `string` | no |
| `filter` | query | `string` | no |
| `fromStartTime` | query | `string` | no |
| `level` | query | `string` | no |
| `name` | query | `string` | no |
| `parentObservationId` | query | `string` | no |
| `parseIoAsJson` | query | `string` | no |
| `toStartTime` | query | `string` | no |
| `traceId` | query | `string` | no |
| `type` | query | `string` | no |
| `userId` | query | `string` | no |
| `version` | query | `string` | no |
