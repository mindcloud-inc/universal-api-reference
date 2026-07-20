# Share Checklist with CheckFlow

## Endpoint

- **Method:** `POST`
- **Path:** `/api/checklist/share`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [Share Checklist](https://docs.checkflow.io/docs/api/checklists#share-checklist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checklistId` | query | `number` | yes | The ID of the checklist. |
| `isShared` | query | `boolean` | yes | Use true to create a share URL and false to remove it. |
