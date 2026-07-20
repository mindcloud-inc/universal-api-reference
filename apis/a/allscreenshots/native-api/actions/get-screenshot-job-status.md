# Get Screenshot Job Status with Allscreenshots

Retrieves the status of an async screenshot job in Allscreenshots.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/screenshots/jobs/:jobId`
- **Base URL:** `https://api.allscreenshots.com`
- **Official documentation:** [Get Screenshot Job Status](https://docs.allscreenshots.com/api-reference/async-jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | The async screenshot job to inspect. |
