# Create Field with Audienceful

Creates a new custom field in Audienceful.

## Endpoint

- **Method:** `POST`
- **Path:** `/people/fields/`
- **Base URL:** `https://app.audienceful.com/api`
- **Official documentation:** [Create Field](https://developer.audienceful.com/api-reference/fields/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Human-readable field name. |
| `data_name` | body | `string` | yes | Field key used in person payloads. |
| `type` | body | `string` | yes | Field data type. |
| `editable` | body | `boolean` | no | Whether the field can be edited. |
| `required` | body | `boolean` | no | Whether the field is required. |
