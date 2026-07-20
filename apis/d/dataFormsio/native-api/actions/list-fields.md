# List Fields with DataForms.io

Retrieves fields from DataForms.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/templates/{template_id}/fields`
- **Base URL:** `https://api.dataforms.io`
- **Official documentation:** [List Fields](https://dataforms.readme.io/reference/index-fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | path | `string` | yes | The DataForms.io template identifier. |
| `search` | query | `string` | no | Filter fields by search term. |
