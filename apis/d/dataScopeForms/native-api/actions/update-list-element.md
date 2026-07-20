# Update List Element with DataScope Forms

Updates an existing list element in DataScope Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/external/metadata_object/[:id]`
- **Base URL:** `https://www.mydatascope.com/api`
- **Official documentation:** [Update List Element](https://dscope.github.io/docs/#update-a-list-element)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Internal identifier of the list element to update. |
| `list_object.attribute1` | body | `string` | no | First custom attribute of the list element. |
| `list_object.attribute2` | body | `string` | no | Second custom attribute of the list element. |
| `list_object.code` | body | `string` | no | Internal code of the list element. |
| `list_object.description` | body | `string` | no | Description of the list element. |
| `list_object.name` | body | `string` | no | Name of the list element. |
