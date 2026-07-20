# Update Collection Record with Zixflow

Updates an existing collection record in Zixflow.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/collection-records/:collectionId/:recordId`
- **Base URL:** `https://api.zixflow.com/api/v1`
- **Official documentation:** [Update Collection Record](https://docs.zixflow.com/api-reference/records/edit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Collection identifier. |
| `recordId` | path | `string` | yes | Record identifier. |
