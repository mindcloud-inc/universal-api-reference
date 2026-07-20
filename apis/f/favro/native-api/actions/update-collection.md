# Update Collection with Favro

Updates an existing collection in Favro.

## Endpoint

- **Method:** `PUT`
- **Path:** `/collections/:collectionId`
- **Base URL:** `https://favro.com/api/v1`
- **Official documentation:** [Update Collection](https://favro.com/developer/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | The Favro collection ID to update. |
| `name` | body | `string` | yes | The new collection name. Maximum length: 48. |
