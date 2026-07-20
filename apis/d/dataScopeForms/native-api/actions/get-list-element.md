# Get List Element with DataScope Forms

Retrieves a list element from DataScope Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/external/metadata_object`
- **Base URL:** `https://www.mydatascope.com/api`
- **Official documentation:** [Get List Element](https://dscope.github.io/docs/#get-an-element-of-the-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `metadata_id` | query | `number` | no | Internal identifier of the list element to fetch. |
| `metadata_type` | query | `string` | no | Internal code that identifies the target list. |
