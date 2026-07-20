# Create List Element with DataScope Forms

Creates a new list element in DataScope Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/external/metadata_object`
- **Base URL:** `https://www.mydatascope.com/api`
- **Official documentation:** [Create List Element](https://dscope.github.io/docs/#create-a-list-element)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_object.attribute1` | body | `string` | no | First custom attribute of the list element. |
| `list_object.attribute2` | body | `string` | no | Second custom attribute of the list element. |
| `list_object.code` | body | `string` | no | Internal code of the list element. |
| `list_object.description` | body | `string` | no | Description of the list element. |
| `list_object.name` | body | `string` | no | Name of the list element. |
| `metadata_type` | query | `string` | no | Internal code that identifies the target list. |
