# Query Retention Report with Mixpanel

Retrieves a retention report from Mixpanel.

## Endpoint

- **Method:** `GET`
- **Path:** `/query/retention`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [Query Retention Report](https://developer.mixpanel.com/reference/retention-query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `number` | no | Required when authenticating with a Mixpanel service account. |
| `workspace_id` | query | `number` | no | Optional Mixpanel workspace ID. |
| `from_date` | query | `string` | yes | Inclusive start date in YYYY-MM-DD format. |
| `to_date` | query | `string` | yes | Inclusive end date in YYYY-MM-DD format. |
| `retention_type` | query | `string` | no | Retention mode: birth or compounded. |
| `born_event` | query | `string` | no | First event for birth-retention cohorts. |
| `event` | query | `string` | no | Event to count as returning activity. |
| `born_where` | query | `string` | no | Filter expression for the born event. |
| `where` | query | `string` | no | Filter expression for returning events. |
| `interval` | query | `number` | no | Bucket size for retention intervals. |
| `interval_count` | query | `number` | no | Number of intervals to return. |
| `unit` | query | `string` | no | Interval unit: day, week, or month. |
| `unbounded_retention` | query | `boolean` | no | Accumulate retention counts from right to left when true. |
| `on` | query | `string` | no | Property expression used to segment returning events. |
| `limit` | query | `number` | no | Maximum number of segmentation values to return when using `on`. |
