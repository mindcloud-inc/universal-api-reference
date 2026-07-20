# Batch Delete Jobs with Detrack

Deletes multiple jobs from Detrack at once.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/dn/jobs`
- **Base URL:** `https://app.detrack.com/api/v2`
- **Official documentation:** [Batch Delete Jobs](https://detrackapiv2.docs.apiary.io/#reference/jobs/batch-update-delete/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Array of job identity objects to delete. Use Detrack job ids for the most reliable batch delete behavior. |
