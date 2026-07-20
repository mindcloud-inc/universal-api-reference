# Delete File with Instant

Deletes a file from Instant storage.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/admin/storage/files`
- **Base URL:** `https://api.instantdb.com`
- **Official documentation:** [Delete File](https://www.instantdb.com/docs/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | query | `string` | yes | Stored file path to delete. |
