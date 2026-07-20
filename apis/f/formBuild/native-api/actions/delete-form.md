# Delete Form with 123FormBuild

Deletes an existing form from 123FormBuilder.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/forms/{form_id}`
- **Base URL:** `https://api.123formbuilder.com/v2`
- **Official documentation:** [Delete Form](https://www.123formbuilder.com/developer/api-v2-forms/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | path | `number` | yes | The ID of the form |
