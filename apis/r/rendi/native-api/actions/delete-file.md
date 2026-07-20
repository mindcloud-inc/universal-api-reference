# Delete File with Rendi

Deletes a stored file from Rendi.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/files/:file_id`
- **Base URL:** `https://api.rendi.dev`
- **Official documentation:** [Delete File](https://docs.rendi.dev/api-reference/endpoint/delete-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | path | `string` | yes | UUID of the stored file to delete. |
