# Query Saved Insights Report with Mixpanel

Retrieves a saved insights report from Mixpanel.

## Endpoint

- **Method:** `GET`
- **Path:** `/query/insights`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [Query Saved Insights Report](https://developer.mixpanel.com/reference/insights-query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `number` | no | Required when authenticating with a Mixpanel service account. |
| `workspace_id` | query | `number` | no | Optional Mixpanel workspace ID. |
| `bookmark_id` | query | `number` | yes | Saved Insights report ID from the Mixpanel URL. |
