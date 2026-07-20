# Batch Delete Files with Uploadcare

Deletes multiple files from Uploadcare storage.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/files/storage/`
- **Base URL:** `https://api.uploadcare.com`
- **Official documentation:** [Batch Delete Files](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/File/operation/filesDelete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuids[]` | body | `array<string>` | yes | List of Uploadcare file UUIDs to delete. |
