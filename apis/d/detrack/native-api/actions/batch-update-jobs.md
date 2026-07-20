# Batch Update Jobs with Detrack

Updates multiple jobs in Detrack at once.

## Endpoint

- **Method:** `PUT`
- **Path:** `/dn/jobs`
- **Base URL:** `https://app.detrack.com/api/v2`
- **Official documentation:** [Batch Update Jobs](https://detrackapiv2.docs.apiary.io/#reference/jobs/batch-update-delete/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Array of job update objects. Each item must include do_number, date, and a nested data object with the fields to update. |
