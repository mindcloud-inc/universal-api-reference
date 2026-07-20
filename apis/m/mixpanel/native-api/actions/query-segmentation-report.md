# Query Segmentation Report with Mixpanel

Retrieves a segmentation report from Mixpanel.

## Endpoint

- **Method:** `GET`
- **Path:** `/query/segmentation`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [Query Segmentation Report](https://developer.mixpanel.com/reference/segmentation-query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `number` | no | Required when authenticating with a Mixpanel service account. |
| `workspace_id` | query | `number` | no | Optional Mixpanel workspace ID. |
| `event` | query | `string` | yes | Single event name to analyze. |
| `from_date` | query | `string` | yes | Inclusive start date in YYYY-MM-DD format. |
| `to_date` | query | `string` | yes | Inclusive end date in YYYY-MM-DD format. |
| `on` | query | `string` | no | Property expression used to segment the event. |
| `unit` | query | `string` | no | Time bucket unit. |
| `interval` | query | `number` | no | Optional bucket interval. |
| `where` | query | `string` | no | Expression used to filter events. |
| `limit` | query | `number` | no | Maximum number of segmentation values to return when using `on`. |
| `type` | query | `string` | no | Aggregation type: general, unique, or average. |
| `format` | query | `string` | no | Optional response format. |
