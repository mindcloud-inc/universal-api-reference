# Remove Tag Assignment with CheckFlow

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/tag/assignment`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [Remove Tag Assignment](https://docs.checkflow.io/docs/api/tags#remove-tag-assignment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tagKey` | body | `string` | yes | The key of the tag assignment to remove. |
| `assignmentKey` | body | `string` | yes | The key of the checklist or task the tag is being removed from. |
| `assignmentType` | body | `number` | yes | 1 for checklist, 3 for task. |
| `parentKey` | body | `string` | no | Required when removing a tag from a task. The checklist key that contains the task. |
