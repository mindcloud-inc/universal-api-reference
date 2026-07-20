# List Annotations with Mixpanel

Retrieves annotations from a Mixpanel project.

## Endpoint

- **Method:** `GET`
- **Path:** `/app/projects/:projectId/annotations`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [List Annotations](https://developer.mixpanel.com/reference/list-all-annotations-for-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | Mixpanel project ID. |
| `fromDate` | query | `string` | no | Inclusive start date in YYYY-MM-DD format. |
| `toDate` | query | `string` | no | Inclusive end date in YYYY-MM-DD format. |
