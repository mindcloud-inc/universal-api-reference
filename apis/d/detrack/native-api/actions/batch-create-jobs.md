# Batch Create Jobs with Detrack

Creates multiple jobs in Detrack at once.

## Endpoint

- **Method:** `POST`
- **Path:** `/dn/jobs/bulk`
- **Base URL:** `https://app.detrack.com/api/v2`
- **Official documentation:** [Batch Create Jobs](https://detrackapiv2.docs.apiary.io/#reference/jobs/batch-create/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Array of job objects to create. Each item should include at least do_number, date, and address; type defaults to Delivery. |
