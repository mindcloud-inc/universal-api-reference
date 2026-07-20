# List Incidents with PagerDuty

## Endpoint

- **Method:** `GET`
- **Path:** `/incidents`
- **Base URL:** `https://api.pagerduty.com`
- **Official documentation:** [List Incidents](https://developer.pagerduty.com/api-reference/listIncidents)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_range` | query | `string` | no | Set to all to ignore the default since and until range. |
| `incident_key` | query | `string` | no | Filter incidents by incident de-duplication key. |
| `service_ids[]` | query | `array<string>` | no | Return only incidents associated with these service IDs. |
| `team_ids[]` | query | `array<string>` | no | Return only incidents related to these team IDs. |
| `user_ids[]` | query | `array<string>` | no | Return only incidents currently assigned to these user IDs. |
| `urgencies[]` | query | `array<string>` | no | Return only incidents with these urgency values. |
| `time_zone` | query | `string` | no | Time zone used when rendering the results. |
| `statuses[]` | query | `array<string>` | no | Return only incidents with these statuses. |
| `include[]` | query | `array<string>` | no | Include additional incident details in the response. |
| `since` | query | `date` | no | Start of the incident search time range. |
| `until` | query | `date` | no | End of the incident search time range. |
