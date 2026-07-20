# Create Asset with Screenly

Creates a new asset in Screenly.

## Endpoint

- **Method:** `POST`
- **Path:** `/assets/`
- **Base URL:** `https://api.screenlyapp.com/api/v3`
- **Official documentation:** [Create Asset](https://developer.screenly.io/api/#assets_create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `disable_verification` | body | `boolean` | no |
| `folder_name` | body | `string` | no |
| `js_injection` | body | `string` | no |
| `source_url` | body | `string` | yes |
| `title` | body | `string` | no |
