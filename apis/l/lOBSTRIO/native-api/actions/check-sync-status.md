# Check Sync Status with LOBSTR.IO

Retrieves sync task status from LOBSTR.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/synchronize/:sync_task_id`
- **Base URL:** `https://api.lobstr.io`
- **Official documentation:** [Check Sync Status](https://docs.lobstr.io/docs/check-sync-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sync_task_id` | path | `string` | yes | The synchronization task ID returned by Sync Account or Refresh Cookies. |
