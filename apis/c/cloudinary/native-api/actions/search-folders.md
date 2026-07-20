# Search Folders with Cloudinary

Finds folders in Cloudinary by search expression.

## Endpoint

- **Method:** `GET`
- **Path:** `/folders/search`
- **Base URL:** `https://api.cloudinary.com/v1_1/{cloudName}`
- **Official documentation:** [Search Folders](https://cloudinary.com/documentation/admin_api#search_folders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `expression` | query | `string` | yes | The folder search expression to run. |
