# List Appointments with Zenoti

## Endpoint

- **Method:** `GET`
- **Path:** `appointments`
- **Base URL:** `https://api.zenoti.com/v1/`
- **Official documentation:** [List Appointments](https://docs.zenoti.com/reference/retrieve-the-list-of-appointments-of-a-center)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `center_id` | query | `list` | yes | — |
| `start_date` | query | `date` | yes | — |
| `end_date` | query | `date` | yes | Retrieves the appointments that have appointment start date before the specified end_date (exclusive of end_date). For example, if you specify start_date as 2020-08-03 and end_date as 2020-08-04, this API will retrieve the list of appointments for only Aug 3, 2020. Note: start_date and end_date must be different. |
| `include_no_show_cancel` | query | `boolean` | no | Format: `toggle`. |
| `therapist_id` | query | `string` | no | Format: `toggle`. |
