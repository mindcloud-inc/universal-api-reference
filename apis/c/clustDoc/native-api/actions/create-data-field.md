# Create Data Field with ClustDoc

## Endpoint

- **Method:** `POST`
- **Path:** `/data-fields`
- **Base URL:** `https://api.clustdoc.com/api`
- **Official documentation:** [Create Data Field](https://clustdoc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Data field name. |
| `parent_type` | body | `string` | yes | Parent resource type for the data field. |
| `type` | body | `string` | yes | Data field type, for example text. |
