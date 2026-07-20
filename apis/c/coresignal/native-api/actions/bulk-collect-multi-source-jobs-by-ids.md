# Bulk Collect Multi-source Jobs By IDs with Coresignal

Creates a bulk multi-source job collection request in Coresignal.

## Endpoint

- **Method:** `POST`
- **Path:** `/data_requests/job_multi_source/ids`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Bulk Collect Multi-source Jobs By IDs](https://docs.coresignal.com/jobs-api/multi-source-jobs-api/bulk-collect)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ids[]` | body | `array<number>` | yes |
