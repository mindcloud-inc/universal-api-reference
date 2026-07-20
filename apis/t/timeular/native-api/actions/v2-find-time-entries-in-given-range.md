# V2 Find Time Entries in given range with Timeular

Retrieves time entries in a date range from the Timeular v2 API.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/time-entries/:start/:end`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [V2 Find Time Entries in given range](https://developers.early.app/#d950b394-7427-4dae-a9f6-472becc07eda)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `end` | path | `string` | yes |
| `start` | path | `string` | yes |
