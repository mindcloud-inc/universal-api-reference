# Add Bucket To Group with EyeLevel.ai

Adds a bucket to a group in EyeLevel.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/group/:groupId/bucket/:bucketId`
- **Base URL:** `https://api.groundx.ai/api/v1`
- **Official documentation:** [Add Bucket To Group](https://docs.eyelevel.ai/reference/api-reference/groups/add-bucket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `number` | yes | The groupId of the group that will receive the bucket. |
| `bucketId` | path | `number` | yes | The bucketId of the bucket to add to the group. |
