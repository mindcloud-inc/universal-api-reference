# Create Template Folder with Superchat

Creates a new template folder in Superchat.

## Endpoint

- **Method:** `POST`
- **Path:** `/template-folders`
- **Base URL:** `https://api.superchat.com/v1.0`
- **Official documentation:** [Create Template Folder](https://developers.superchat.com/reference/createtemplatefolder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the template folder. |
| `parent_id` | body | `string` | no | Unique identifier of the template folder. Always bears prefix 'tn_' |
