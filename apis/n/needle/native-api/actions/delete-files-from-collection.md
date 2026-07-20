# Delete Files From Collection with Needle

Deletes files from a collection in Needle.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/collections/:collectionId/files`
- **Base URL:** `https://needle.app`
- **Official documentation:** [Delete Files From Collection](https://docs.needle.app/docs/api-reference/delete-files-from-collection/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | ID of the collection to delete files from |
| `file_ids[]` | body | `array<string>` | yes | File IDs to remove from the collection |
