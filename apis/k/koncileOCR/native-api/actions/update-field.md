# Update Field with Koncile OCR

## Endpoint

- **Method:** `PUT`
- **Path:** `/update_field`
- **Base URL:** `https://api.koncile.ai/v1`
- **Official documentation:** [Update Field](https://docs.koncile.ai/api-setup/fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `desc` | body | `string` | no | Update the field description. |
| `field_id` | query | `number` | yes | The field identifier to update. |
| `format` | body | `string` | no | Update the field format, such as text. |
| `name` | body | `string` | no | Update the field name. |
| `position` | body | `string` | no | Update the relative position of the field in the output. |
| `type` | body | `string` | no | Update whether the field is General fields or Line fields. |
