# Update Field with BigMailer

Updates an existing field in a BigMailer brand.

## Endpoint

- **Method:** `POST`
- **Path:** `/brands/:brand_id/fields/:field_id`
- **Base URL:** `https://api.bigmailer.io/v1`
- **Official documentation:** [Update Field](https://docs.bigmailer.io/reference/updatefield)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brand_id` | path | `string` | yes | ID of the brand containing the field. |
| `field_id` | path | `string` | yes | ID of the field. |
| `name` | body | `string` | no | Updated display name of the field. |
| `merge_tag_name` | body | `string` | no | Updated merge tag used for the field. |
| `sample_value` | body | `string` | no | Updated sample value for the field. |
