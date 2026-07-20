# List Deltas with Cerbo

Retrieves Cerbo delta changes for a resource type.

## Endpoint

- **Method:** `GET`
- **Path:** `/delta/:resource_type`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Deltas](https://docs.cer.bo/#tag/Deltas/operation/listDeltas)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resource_type` | path | `string` | yes | Resource type. Valid resources include `appointments`, `rxs`, `pt_rx`, `drugs`, `supplements`, `orders`, `pt_orders`, `documents`, `patients`, `users`, `tags`, `pt_tags`, `tasks`. |
| `start_date` | query | `string` | yes | Starting date of the date range. The start date should be formatted as `YYYY-MM-DD`. The start date can also include time, and should be formatted as `YYYY-MM-DD HH:MM:SS`. |
| `end_date` | query | `string` | yes | Ending date of the date range. The end date should be formatted as `YYYY-MM-DD`. The end date can also include time, and should be formatted as `YYYY-MM-DD HH:MM:SS`. The end date must be later than the start date, but can **NOT** be longer than a week in length. |
