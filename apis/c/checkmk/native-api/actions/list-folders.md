# List Folders with Checkmk

Retrieves folder configuration records from Checkmk.

## Endpoint

- **Method:** `GET`
- **Path:** `/domain-types/folder_config/collections/all`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [List Folders](https://docs.checkmk.com/latest/en/rest_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parent` | query | `string` | no | Parent folder slug to start from. Use ~ for Main. |
| `recursive` | query | `boolean` | no | Whether to include nested folders. |
| `show_hosts` | query | `boolean` | no | Whether folder responses should include hosts. |
