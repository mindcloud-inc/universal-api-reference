# Get Profile Event Activity with Mixpanel

Retrieves profile event activity from Mixpanel.

## Endpoint

- **Method:** `GET`
- **Path:** `/query/stream/query`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [Get Profile Event Activity](https://developer.mixpanel.com/reference/activity-stream-query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `number` | no | Required when authenticating with a Mixpanel service account. |
| `workspace_id` | query | `number` | no | Optional Mixpanel workspace ID. |
| `distinct_ids` | query | `string` | yes | JSON array string of distinct IDs to inspect. |
| `from_date` | query | `string` | yes | Inclusive start date in YYYY-MM-DD format. |
| `to_date` | query | `string` | yes | Inclusive end date in YYYY-MM-DD format. |
