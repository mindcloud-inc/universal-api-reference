# List Schedules with Olostep

Retrieves schedules from Olostep.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/schedules`
- **Base URL:** `https://api.olostep.com`
- **Official documentation:** [List Schedules](https://docs.olostep.com/api-reference/schedules/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_deleted` | query | `string` | no | Set to true to include deleted schedules in the response. By default, deleted schedules are filtered out. Accepted values: `0`, `1`. |
