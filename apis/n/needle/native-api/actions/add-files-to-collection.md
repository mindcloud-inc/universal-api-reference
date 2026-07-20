# Add Files To Collection with Needle

Adds files to a collection in Needle.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/collections/:collectionId/files`
- **Base URL:** `https://needle.app`
- **Official documentation:** [Add Files To Collection](https://docs.needle.app/docs/api-reference/add-files-to-collection/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | ID of the collection to add files to |
| `files[].name` | body | `string` | yes | Display name of the file to add |
| `files[].url` | body | `string` | yes | URL of the file to add to the collection |
