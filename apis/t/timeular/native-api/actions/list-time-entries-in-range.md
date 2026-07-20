# List Time Entries in Range with Timeular

Retrieves time entries in a date range from your Timeular workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v4/time-entries/:start/:end`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [List Time Entries in Range](https://developers.early.app/#98b4f754-ebcd-4706-b9b0-93244c24e033)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `end` | path | `string` | yes |
| `start` | path | `string` | yes |
