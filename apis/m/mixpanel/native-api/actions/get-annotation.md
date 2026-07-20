# Get Annotation with Mixpanel

Retrieves an annotation from Mixpanel.

## Endpoint

- **Method:** `GET`
- **Path:** `/app/projects/:projectId/annotations/:annotationId`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [Get Annotation](https://developer.mixpanel.com/reference/get-annotation-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | Mixpanel project ID. |
| `annotationId` | path | `number` | yes | Annotation ID returned by Mixpanel. |
