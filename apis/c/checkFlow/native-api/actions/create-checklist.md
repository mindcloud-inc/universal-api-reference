# Create Checklist with CheckFlow

## Endpoint

- **Method:** `POST`
- **Path:** `/api/checklist`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [Create Checklist](https://docs.checkflow.io/docs/api/checklists#create-checklist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateKey` | query | `string` | yes | The key of the template the checklist is derived from. |
| `checklistName` | query | `string` | yes | The name for the new checklist. |
