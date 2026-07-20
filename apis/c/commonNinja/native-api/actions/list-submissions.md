# List Submissions with Common Ninja

Retrieves project submissions from Common Ninja.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/submissions`
- **Base URL:** `https://api.commoninja.com/platform/api/v1`
- **Official documentation:** [List Submissions](https://developers.commoninja.com/docs/api/crm/submissions-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The project ID. |
| `limit` | query | `number` | no | Maximum number of submissions to return. |
| `widgetId` | query | `string` | no | Filter submissions by widget ID. |
