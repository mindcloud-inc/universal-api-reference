# Get Folder Ancestors with Erase.bg

Retrieves folder ancestors from Erase.bg storage.

## Endpoint

- **Method:** `GET`
- **Path:** `/service/platform/assets/v1.0/folders/:_id/ancestors`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Get Folder Ancestors](https://www.pixelbin.io/docs/storage/miscellaneous/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_id` | path | `string` | yes | Folder _id to inspect ancestors for. |
