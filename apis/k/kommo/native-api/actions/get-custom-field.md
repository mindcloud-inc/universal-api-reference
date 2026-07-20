# Get Custom Field with Kommo

## Endpoint

- **Method:** `GET`
- **Path:** `/:entity_type/custom_fields/:id`
- **Base URL:** `https://{referer}/api/v4`
- **Official documentation:** [Get Custom Field](https://developers.kommo.com/reference/custom-fields-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_type` | path | `string` | yes | The entity type segment used in the path. |
| `entity_type` | path | `string` | no | Required path parameter for Get Custom Field. |
| `id` | path | `number` | yes | The custom field identifier. |
