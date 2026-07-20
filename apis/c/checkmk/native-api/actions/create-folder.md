# Create Folder with Checkmk

Creates a new folder in Checkmk.

## Endpoint

- **Method:** `POST`
- **Path:** `/domain-types/folder_config/collections/all`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [Create Folder](https://docs.checkmk.com/latest/en/rest_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Folder internal name. |
| `title` | body | `string` | yes | Folder display title. |
| `parent` | body | `string` | yes | Parent folder slug. Use ~ for Main. |
| `attributes` | body | `object` | no | Optional folder attributes object. |
