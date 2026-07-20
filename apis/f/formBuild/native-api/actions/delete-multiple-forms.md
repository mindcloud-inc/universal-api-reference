# Delete Multiple Forms with 123FormBuild

Deletes multiple forms from your 123FormBuilder account.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/forms/bulk`
- **Base URL:** `https://api.123formbuilder.com/v2`
- **Official documentation:** [Delete Multiple Forms](https://www.123formbuilder.com/developer/api-v2-forms/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_ids` | body | `string` | yes | Comma-separated IDs of the forms to delete |
