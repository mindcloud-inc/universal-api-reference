# Get Collection Record By ID with Zixflow

Retrieves a collection record from Zixflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/collection-records/:collectionId/:recordId`
- **Base URL:** `https://api.zixflow.com/api/v1`
- **Official documentation:** [Get Collection Record By ID](https://docs.zixflow.com/api-reference/records/get-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Collection identifier. |
| `recordId` | path | `string` | yes | Record identifier. |
