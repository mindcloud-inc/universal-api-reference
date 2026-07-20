# List Estimates with Housecall Pro

## Endpoint

- **Method:** `GET`
- **Path:** `/estimates`
- **Base URL:** `https://api.housecallpro.com`
- **Official documentation:** [List Estimates](https://docs.housecallpro.com/docs/housecall-public-api/e430ba3d520a0)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scheduled_start_min` | query | `date` | no | Filters estimates with a starting time greater than or equal to the date sent. |
| `scheduled_start_max` | query | `date` | no | Filters estimates with a starting time less than or equal to the date sent. |
| `scheduled_end_min` | query | `date` | no | Filters estimates with an end time greater than or equal to the date sent. |
| `scheduled_end_max` | query | `date` | no | Filters estimates with an end time less than or equal to the date sent. |
| `employee_ids[]` | query | `array<string>` | no | Filters estimates by assigned pro id. Send multiple values as a array. |
| `customer_id` | query | `string` | no | Filters estimates by a single customer ID. |
| `work_status` | query | `list<string>` | no | Work status filter. Returns estimates from all statuses if empty. Accepted values: `canceled`, `completed`, `in_progress`, `scheduled`, `unscheduled`. Send multiple values as a array. |
| `location_ids[]` | query | `array<string>` | no | IDs of locations you want to pull from. Send multiple values as a array. |
| `expand` | query | `list<string>` | no | Array of strings to expand response body. Accepted values: `attachments`. Send multiple values as a array. |
