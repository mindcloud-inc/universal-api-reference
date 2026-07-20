# Assign Tag To Checklist Or Task with CheckFlow

## Endpoint

- **Method:** `POST`
- **Path:** `/api/tag/assignment`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [Assign Tag To Checklist Or Task](https://docs.checkflow.io/docs/api/tags#assign-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tagKey` | body | `string` | yes | The key of the tag to assign. |
| `assignmentKey` | body | `string` | yes | The key of the checklist or task the tag is being assigned to. |
| `assignmentType` | body | `number` | yes | 1 for checklist, 3 for task. |
| `parentKey` | body | `string` | no | Required when assigning a tag to a task. The checklist key that contains the task. |
