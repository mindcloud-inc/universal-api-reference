# Update Collection with Dubble

Updates an existing collection in Dubble.

## Endpoint

- **Method:** `PUT`
- **Path:** `/collections/:collectionId`
- **Base URL:** `https://api.dubble.so/v1`
- **Official documentation:** [Update Collection](https://dubble.readme.io/reference/updatecollection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | The ID of the collection |
| `name` | body | `string` | no | The updated collection name |
| `visibility` | body | `string` | no | The updated visibility setting for the collection |
