# Update Asset with Screenly

Updates an existing asset in Screenly.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/assets/:id/`
- **Base URL:** `https://api.screenlyapp.com/api/v3`
- **Official documentation:** [Update Asset](https://developer.screenly.io/api/#assets_partial_update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `folder_name` | body | `string` | no |
| `id` | path | `string` | yes |
| `js_injection` | body | `string` | no |
| `title` | body | `string` | no |
