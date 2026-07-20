# List Saved Cohorts with Mixpanel

Retrieves saved cohorts from Mixpanel.

## Endpoint

- **Method:** `POST`
- **Path:** `/query/cohorts/list`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [List Saved Cohorts](https://developer.mixpanel.com/reference/cohorts-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `number` | no | Required when using service-account authentication for the Query API. |
| `workspace_id` | query | `number` | no | Optional workspace ID when the cohort lives in a workspace context. |
