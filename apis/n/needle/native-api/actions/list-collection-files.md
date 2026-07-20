# List Collection Files with Needle

Retrieves files from a Needle collection.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/collections/:collectionId/files`
- **Base URL:** `https://needle.app`
- **Official documentation:** [List Collection Files](https://docs.needle.app/docs/api-reference/list-collection-files/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | ID of the collection whose files will be listed |
