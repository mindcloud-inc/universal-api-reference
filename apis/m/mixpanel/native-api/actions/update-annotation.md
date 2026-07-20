# Update Annotation with Mixpanel

Updates an existing annotation in Mixpanel.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/app/projects/:projectId/annotations/:annotationId`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [Update Annotation](https://developer.mixpanel.com/reference/patch-annotation-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | Mixpanel project ID. |
| `annotationId` | path | `number` | yes | Annotation ID returned by Mixpanel. |
| `description` | body | `string` | no | Updated annotation text. |
| `tags` | body | `list<number>` | no | Replacement list of Mixpanel annotation tag IDs. |
