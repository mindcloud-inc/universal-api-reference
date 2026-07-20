# Get Field with BigMailer

Retrieves a field from a BigMailer brand.

## Endpoint

- **Method:** `GET`
- **Path:** `/brands/:brand_id/fields/:field_id`
- **Base URL:** `https://api.bigmailer.io/v1`
- **Official documentation:** [Get Field](https://docs.bigmailer.io/reference/getfield)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brand_id` | path | `string` | yes | ID of the brand containing the field. |
| `field_id` | path | `string` | yes | ID of the field. |
