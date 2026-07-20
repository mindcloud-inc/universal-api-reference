# Get Bulk Job Status with Allscreenshots

Retrieves the status of a bulk screenshot job in Allscreenshots.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/screenshots/bulk/:bulkJobId`
- **Base URL:** `https://api.allscreenshots.com`
- **Official documentation:** [Get Bulk Job Status](https://docs.allscreenshots.com/api-reference/bulk)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bulkJobId` | path | `string` | yes | The bulk screenshot job to inspect. |
