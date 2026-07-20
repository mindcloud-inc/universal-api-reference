# Delete Files in Bulk with Rendi

Deletes multiple stored files from Rendi.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/files/bulk-delete`
- **Base URL:** `https://api.rendi.dev`
- **Official documentation:** [Delete Files in Bulk](https://docs.rendi.dev/api-reference/endpoint/delete-files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_ids` | body | `object<string>` | yes | Array of file UUIDs to delete (1-1000 items). |
