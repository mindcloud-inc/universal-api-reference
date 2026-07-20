# Get Field with DataForms.io

Retrieves a field from DataForms.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/templates/{template_id}/fields/{field_id}`
- **Base URL:** `https://api.dataforms.io`
- **Official documentation:** [Get Field](https://dataforms.readme.io/reference/index-fields-copy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | path | `string` | yes | The DataForms.io template identifier. |
| `field_id` | path | `string` | yes | The DataForms.io field identifier. |
