# Export Events with Mixpanel

Retrieves raw events from Mixpanel.

## Endpoint

- **Method:** `GET`
- **Path:** `https://data.mixpanel.com/api/2.0/export`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [Export Events](https://developer.mixpanel.com/reference/raw-event-export)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_date` | query | `string` | yes | Inclusive start date in YYYY-MM-DD format. |
| `to_date` | query | `string` | yes | Inclusive end date in YYYY-MM-DD format. |
| `limit` | query | `number` | no | Optional maximum number of events to return; cannot exceed 100000. |
| `event` | query | `string` | no | Optional JSON-encoded array of event names to export. |
| `where` | query | `string` | no | Optional Mixpanel expression used to filter exported events. |
| `project_id` | query | `number` | no | Required if using service account authentication for this request. |
| `time_in_ms` | query | `boolean` | no | Return timestamps in milliseconds when true. |
