# Create a new template with CraftMyPDF

Creates a new template in CraftMyPDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/new-template-from`
- **Base URL:** `https://api.craftmypdf.com/v1`
- **Official documentation:** [Create a new template](https://craftmypdf.com/docs/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `template_id` | body | `string` | yes |
| `name` | body | `string` | no |
| `version` | body | `string` | no |
| `group_name` | body | `string` | no |
