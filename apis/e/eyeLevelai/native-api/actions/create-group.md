# Create Group with EyeLevel.ai

Creates a new group in EyeLevel.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/group`
- **Base URL:** `https://api.groundx.ai/api/v1`
- **Official documentation:** [Create Group](https://docs.eyelevel.ai/reference/api-reference/groups/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the group being created. |
| `bucketName` | body | `string` | no | Optionally create a bucket with this name and attach it to the new group. |
