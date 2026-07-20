# Lookup Documents with EyeLevel.ai

Retrieves documents in EyeLevel.ai by process, bucket, or group.

## Endpoint

- **Method:** `GET`
- **Path:** `/ingest/documents/:id`
- **Base URL:** `https://api.groundx.ai/api/v1`
- **Official documentation:** [Lookup Documents](https://docs.eyelevel.ai/reference/api-reference/documents/lookup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | A processId, bucketId, or groupId whose associated documents should be listed. |
| `n` | query | `number` | no | The maximum number of returned documents. |
