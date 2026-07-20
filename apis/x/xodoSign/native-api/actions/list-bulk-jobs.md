# List Bulk Jobs with Xodo Sign

Retrieves bulk jobs from Xodo Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/bulk_job`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [List Bulk Jobs](https://eversign.com/api/documentation/methods#get-bulk-jobs-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | query | `string` | yes | The Xodo Sign business ID that owns the bulk jobs. |
| `limit` | query | `number` | no | Maximum amount of jobs to fetch. |
| `offset` | query | `number` | no | Number of jobs to skip when fetching results. |
