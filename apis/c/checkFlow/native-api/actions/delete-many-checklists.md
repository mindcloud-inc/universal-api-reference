# Delete Many Checklists with CheckFlow

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/checklist/delete-many`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [Delete Many Checklists](https://docs.checkflow.io/docs/api/checklists#delete-many-checklists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checklistIds[]` | body | `array<number>` | no | A list of specific checklist IDs to delete. |
| `templateKeys[]` | body | `array<string>` | no | Template keys whose matching checklists should be deleted. |
| `checklistStatus` | body | `string` | no | Status filter used when deleting by template keys. |
