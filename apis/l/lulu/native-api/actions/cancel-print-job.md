# Cancel Print Job with Lulu

Cancels a print job in Lulu.

## Endpoint

- **Method:** `PUT`
- **Path:** `/print-jobs/{id}/status/`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Cancel Print Job](https://api.lulu.com/docs/#tag/Print-Jobs/operation/Print-Jobs_status_cancel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Lulu print job ID. |
