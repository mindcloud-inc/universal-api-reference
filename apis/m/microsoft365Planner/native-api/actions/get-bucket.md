# Get Bucket with Microsoft 365 Planner

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/planner/buckets/{{bucketId}}`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Get Bucket](https://learn.microsoft.com/en-us/graph/api/plannerbucket-get?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketId` | path | `string` | yes | Planner bucket ID to retrieve. |
