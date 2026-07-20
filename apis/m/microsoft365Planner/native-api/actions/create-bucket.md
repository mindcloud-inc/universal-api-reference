# Create Bucket with Microsoft 365 Planner

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/planner/buckets`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Create Bucket](https://learn.microsoft.com/en-us/graph/api/planner-post-buckets?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name for the new Planner bucket. |
| `planId` | body | `string` | yes | Planner plan ID where the bucket should be created. |
