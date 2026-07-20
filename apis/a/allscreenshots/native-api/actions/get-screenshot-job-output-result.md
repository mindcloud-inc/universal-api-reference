# Get Screenshot Job Output Result with Allscreenshots

Retrieves a specific output from an async screenshot job in Allscreenshots.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/screenshots/jobs/:jobId/result/:outputId`
- **Base URL:** `https://api.allscreenshots.com`
- **Official documentation:** [Get Screenshot Job Output Result](https://docs.allscreenshots.com/api-reference/outputs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | The async screenshot job whose specific output you want to download. |
| `outputId` | path | `string` | yes | The output identifier from a multi-output job result. |
