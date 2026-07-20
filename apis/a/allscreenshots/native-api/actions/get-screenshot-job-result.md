# Get Screenshot Job Result with Allscreenshots

Retrieves the completed result of an async screenshot job in Allscreenshots.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/screenshots/jobs/:jobId/result`
- **Base URL:** `https://api.allscreenshots.com`
- **Official documentation:** [Get Screenshot Job Result](https://docs.allscreenshots.com/api-reference/async-jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | The async screenshot job whose result you want to download. |
