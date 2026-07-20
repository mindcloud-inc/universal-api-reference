# Get Print Job Status with Lulu

Retrieves the status of a print job from Lulu.

## Endpoint

- **Method:** `GET`
- **Path:** `/print-jobs/{id}/status/`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Get Print Job Status](https://api.lulu.com/docs/#tag/Print-Jobs/operation/Print-Jobs_status_read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Lulu print job ID. |
