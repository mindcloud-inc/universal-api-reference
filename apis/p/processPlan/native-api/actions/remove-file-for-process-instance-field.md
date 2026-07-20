# Remove File for Process Instance Field with Process Plan

## Endpoint

- **Method:** `POST`
- **Path:** `/process_instance_field/:processInstanceFieldId/file/:fileId/remove`
- **Base URL:** `https://apius0.processplan.com/api/v4`
- **Official documentation:** [Remove File for Process Instance Field](https://answers.processplan.com/c/api/api-endpoints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileId` | path | `string` | no | File ID. |
| `processInstanceFieldId` | path | `string` | no | Process instance field ID. |
