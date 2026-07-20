# Create List with DataScope Forms

Creates a new list in DataScope Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/external/metadata_types`
- **Base URL:** `https://www.mydatascope.com/api`
- **Official documentation:** [Create List](https://dscope.github.io/docs/#create-a-empty-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list.code` | body | `string` | no | Internal code of the list. |
| `list.description` | body | `string` | no | Description of the list. |
| `list.list_type` | body | `string` | no | Type of the list. Valid values: standard, percent, price. |
| `list.name` | body | `string` | no | Name of the list. |
