# Update Bucket with EyeLevel.ai

Updates an existing bucket in EyeLevel.ai.

## Endpoint

- **Method:** `PUT`
- **Path:** `/bucket/:bucketId`
- **Base URL:** `https://api.groundx.ai/api/v1`
- **Official documentation:** [Update Bucket](https://docs.eyelevel.ai/reference/api-reference/buckets/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketId` | path | `number` | yes | The bucketId of the bucket being updated. |
| `newName` | body | `string` | yes | The new name of the bucket being renamed. |
