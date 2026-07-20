# Bulk Update List Elements with DataScope Forms

Updates list elements in DataScope Forms by replacing the full list.

## Endpoint

- **Method:** `POST`
- **Path:** `/external/metadata_objects/bulk_update`
- **Base URL:** `https://www.mydatascope.com/api`
- **Official documentation:** [Bulk Update List Elements](https://dscope.github.io/docs/#bulk-update-list-elements)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_objects[]` | body | `array<object>` | yes | Array of list objects to create or update. Objects not present may be soft-deleted by DataScope. |
| `metadata_type` | body | `string` | yes | Internal code that identifies the list to replace. |
| `name` | body | `string` | yes | Name of the list to create or update. |
