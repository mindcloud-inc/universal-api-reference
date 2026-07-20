# List Appointments with Cerbo

Retrieves appointment records from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/appointments`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Appointments](https://docs.cer.bo/#tag/Appointments/operation/listAppointments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | yes | Starting date of the date range. The start date should be formatted as `YYYY-MM-DD`. |
| `status[]` | query | `string` | no | Appointment status. If specified, results will be for only the given statuses. Valid statuses include `scheduled`, `confirmed`, `checked-in`, `in-room`, `cancelled`. Clinic custom statuses may also be used. |
| `end_date` | query | `string` | yes | Ending date of the date range. The end date should be formatted as `YYYY-MM-DD`. |
| `provider_id` | query | `number` | no | Provider identifier. If specified, results will be for only that provider. |
| `pt_id` | query | `number` | no | Patient identifier. If specified, results will be for only that patient. |
| `include_cancelled` | query | `string` | no | If specified and not empty, results will include cancelled appointments. Any non-empty value is treated as true. |
| `include_work_schedule` | query | `string` | no | Include details about when a provider is set to work. Any non-empty value is treated as true. |
