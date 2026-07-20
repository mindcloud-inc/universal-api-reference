# List Time Entries in Range with EARLY

Retrieves time entries from EARLY in a date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v4/time-entries/:start/:end`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [List Time Entries in Range](https://developers.early.app/#98b4f754-ebcd-4706-b9b0-93244c24e033)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | path | `string` | yes | Range start timestamp in EARLY format, for example 2016-01-01T00:00:00.000. |
| `end` | path | `string` | yes | Range end timestamp in EARLY format, for example 2017-12-31T23:59:59.999. |
