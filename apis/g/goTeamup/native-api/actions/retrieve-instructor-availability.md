# Retrieve Instructor Availability with GoTeamup

Retrieves instructor availability from GoTeamup.

## Endpoint

- **Method:** `GET`
- **Path:** `/instructors/:id/availability`
- **Base URL:** `https://goteamup.com/api/v2`
- **Official documentation:** [Retrieve Instructor Availability](https://docs.goteamup.com/api-reference/endpoints/instructors-availability)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_date` | query | `string` | yes | End date for the availability window. |
| `id` | path | `number` | yes | The TeamUp instructor ID. |
| `start_date` | query | `string` | yes | Start date for the availability window. |
