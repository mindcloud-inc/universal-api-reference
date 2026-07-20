# Create Field with BigMailer

Creates a new field in a BigMailer brand.

## Endpoint

- **Method:** `POST`
- **Path:** `/brands/:brand_id/fields`
- **Base URL:** `https://api.bigmailer.io/v1`
- **Official documentation:** [Create Field](https://docs.bigmailer.io/reference/createfield)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brand_id` | path | `string` | yes | ID of the brand to create the field in. |
| `name` | body | `string` | yes | Display name of the field. |
| `merge_tag_name` | body | `string` | no | Merge tag used for the field. |
| `sample_value` | body | `string` | no | Sample value for the field. |
| `type` | body | `string` | yes | Data type of the field. |
