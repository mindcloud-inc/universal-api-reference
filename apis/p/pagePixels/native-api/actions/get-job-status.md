# Get Job Status with PagePixels

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs/:job_id`
- **Base URL:** `https://api.pagepixels.com`
- **Official documentation:** [Get Job Status](https://pagepixels.com/app/screenshots-api-documentation#scheduled-screenshots-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | The PagePixels job ID returned by create or capture endpoints. |
