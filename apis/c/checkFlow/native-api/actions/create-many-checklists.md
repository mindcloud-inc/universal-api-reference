# Create Many Checklists with CheckFlow

## Endpoint

- **Method:** `POST`
- **Path:** `/api/checklist/create-many`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [Create Many Checklists](https://docs.checkflow.io/docs/api/checklists#create-many-checklists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateKey` | body | `string` | yes | The key of the template to create checklists from. |
| `checklistNames[]` | body | `array<string>` | yes | The names of the new checklists to create. |
