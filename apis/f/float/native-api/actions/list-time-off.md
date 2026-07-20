# List Time Off with Float

Retrieves time off entries from Float.

## Endpoint

- **Method:** `GET`
- **Path:** `/timeoffs`
- **Base URL:** `https://api.float.com/v3`
- **Official documentation:** [List Time Off](https://developer.float.com/api_reference.html#Time_Off)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | no | Start of date range in format YYYY-MM-DD |
| `end_date` | query | `string` | no | End of date range in format YYYY-MM-DD |
| `full_day` | query | `number` | no | Filter only on whether time off is full day |
| `status` | query | `number` | no | Filter on the status of the time off |
| `timeoff_type_id` | query | `number` | no | Filter on the ID of the time off type |
| `modified_since` | query | `string` | no | Filter on records with an equal or later modified timestamp |
| `fields` | query | `string` | no | Comma-delimited set of fields to include in the response |
