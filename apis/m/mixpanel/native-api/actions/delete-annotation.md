# Delete Annotation with Mixpanel

Deletes an existing annotation from Mixpanel.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/app/projects/:projectId/annotations/:annotationId`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [Delete Annotation](https://developer.mixpanel.com/reference/delete-annotation-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | Mixpanel project ID. |
| `annotationId` | path | `number` | yes | Annotation ID returned by Mixpanel. |
