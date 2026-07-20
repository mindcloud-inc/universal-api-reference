# Delete Collection Record By ID with Zixflow

Deletes an existing collection record from Zixflow.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/collection-records/:collectionId/:recordId`
- **Base URL:** `https://api.zixflow.com/api/v1`
- **Official documentation:** [Delete Collection Record By ID](https://docs.zixflow.com/api-reference/records/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Collection identifier. |
| `recordId` | path | `string` | yes | Record identifier. |
