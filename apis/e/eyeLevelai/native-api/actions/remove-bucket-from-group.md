# Remove Bucket From Group with EyeLevel.ai

Removes a bucket from a group in EyeLevel.ai.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/group/:groupId/bucket/:bucketId`
- **Base URL:** `https://api.groundx.ai/api/v1`
- **Official documentation:** [Remove Bucket From Group](https://docs.eyelevel.ai/reference/api-reference/groups/remove-bucket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `number` | yes | The groupId of the group that currently contains the bucket. |
| `bucketId` | path | `number` | yes | The bucketId of the bucket to remove from the group. |
