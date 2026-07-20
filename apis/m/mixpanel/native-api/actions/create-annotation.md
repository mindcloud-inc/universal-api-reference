# Create Annotation with Mixpanel

Creates a new annotation in Mixpanel.

## Endpoint

- **Method:** `POST`
- **Path:** `/app/projects/:projectId/annotations`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [Create Annotation](https://developer.mixpanel.com/reference/create-annotation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | Mixpanel project ID. |
| `date` | body | `string` | yes | Annotation timestamp in YYYY-MM-DD HH:mm:ss format. |
| `description` | body | `string` | yes | Annotation text shown in Mixpanel. |
| `tags` | body | `list<number>` | no | Optional list of Mixpanel annotation tag IDs. |
