# Create Field with Baserow

Creates a new field in Baserow.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/database/fields/table/:table_id/`
- **Base URL:** `https://api.baserow.io`
- **Official documentation:** [Create Field](https://api.baserow.io/api/redoc/#operation/create_database_table_field)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `number` | yes | The Baserow table where the field will be created. |
| `name` | body | `string` | yes | The field name. |
| `type` | body | `string` | yes | The Baserow field type slug, for example text, date, boolean, or password. |
| `description` | body | `string` | no | Optional field description. |
| `db_index` | body | `boolean` | no | Whether to add a database index for the field. |
| `allow_endpoint_authentication` | body | `boolean` | no | Enable password-field authentication for password fields. |
