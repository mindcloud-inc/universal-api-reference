# Query Funnel Report with Mixpanel

Retrieves a funnel report from Mixpanel.

## Endpoint

- **Method:** `GET`
- **Path:** `/query/funnels`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [Query Funnel Report](https://developer.mixpanel.com/reference/funnels-query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `number` | no | Required when authenticating with a Mixpanel service account. |
| `workspace_id` | query | `number` | no | Optional Mixpanel workspace ID. |
| `funnel_id` | query | `number` | yes | Saved funnel ID from Mixpanel. |
| `from_date` | query | `string` | yes | Inclusive start date in YYYY-MM-DD format. |
| `to_date` | query | `string` | yes | Inclusive end date in YYYY-MM-DD format. |
| `length` | query | `number` | no | Optional funnel completion window length. |
| `length_unit` | query | `string` | no | Unit for the funnel completion window length. |
| `interval` | query | `number` | no | Optional bucket size in days. |
| `unit` | query | `string` | no | Bucket unit: day, week, or month. |
| `on` | query | `string` | no | Property expression to segment the funnel on. |
| `where` | query | `string` | no | Expression used to filter funnel events. |
| `limit` | query | `number` | no | Maximum number of segmentation values to return when using `on`. |
