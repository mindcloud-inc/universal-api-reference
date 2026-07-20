# Create Custom Field with respond.io

Creates a new custom field in respond.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/space/custom_field`
- **Base URL:** `https://api.respond.io/v2`
- **Official documentation:** [Create Custom Field](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/space-api.yml/paths/~1space~1custom_field/post?fromExportButton=true&snapshotType=http_operation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `allowedValues` | body | `string` | no | Allowed values for select-type fields. |
| `dataType` | body | `string` | yes | Custom field data type. |
| `description` | body | `string` | no | Custom field description. |
| `name` | body | `string` | yes | Custom field name. |
| `slug` | body | `string` | no | Unique custom field slug. |
