# Delete Files with Instant

Deletes multiple files from Instant storage.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/storage/files/delete`
- **Base URL:** `https://api.instantdb.com`
- **Official documentation:** [Delete Files](https://www.instantdb.com/docs/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filenames[]` | body | `array<string>` | yes | Stored file paths to delete. |
