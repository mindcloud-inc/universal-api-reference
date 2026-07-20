# List Jobs with Housecall Pro

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs`
- **Base URL:** `https://api.housecallpro.com`
- **Official documentation:** [List Jobs](https://docs.housecallpro.com/docs/housecall-public-api/6c97704da8bf3-get-jobs)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | query | `string` | no | Filters jobs by a single customer ID. |
| `work_status` | query | `list` | no | Returns jobs from selected work statuses. Accepted values: `canceled`, `completed`, `in_progress`, `scheduled`, `unscheduled`. Send multiple values as a array. |
| `expand` | query | `list` | no | Fields to expand in the response body. Accepted values: `appointments`, `attachments`. Send multiple values as a array. |
| `scheduled_start_min` | query | `date` | no | Filters jobs with a starting time greater than or equal to this date. |
| `scheduled_start_max` | query | `date` | no | Filters jobs with a starting time less than or equal to this date. |
| `scheduled_end_min` | query | `date` | no | Filters jobs with an end time greater than or equal to this date. |
| `scheduled_end_max` | query | `date` | no | Filters jobs with an end time less than or equal to this date. |
| `employee_ids[]` | query | `array<string>` | no | — |
| `location_ids[]` | query | `array<string>` | no | IDs of locations to pull from. Ignored when X-Company-Id is set. |
