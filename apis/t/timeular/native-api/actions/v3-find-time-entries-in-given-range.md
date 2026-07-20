# V3 Find Time Entries in given range with Timeular

Retrieves time entries in a date range from the Timeular v3 API.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/time-entries/:start/:end`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [V3 Find Time Entries in given range](https://developers.early.app/#d4c6e3c4-c38b-4891-aa19-907460f43f9b)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `end` | path | `string` | yes |
| `start` | path | `string` | yes |
