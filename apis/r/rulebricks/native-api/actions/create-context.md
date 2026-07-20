# Create Context with Rulebricks

Creates a new context in Rulebricks.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/contexts`
- **Base URL:** `https://rulebricks.com/api/v1`
- **Official documentation:** [Create Context](https://rulebricks.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auto_execute_decisions` | body | `boolean` | no | Whether bound rules and flows auto-execute |
| `description` | body | `string` | no | Description of the context |
| `history_limit` | body | `number` | no | Maximum number of history entries to retain per field |
| `identity_fact` | body | `string` | yes | Field key used as the unique identifier for instances |
| `name` | body | `string` | yes | Name of the context |
| `on_schema_mismatch` | body | `string` | no | How to handle fields that do not match the schema |
| `schema` | body | `object<object>` | yes | Context schema object. Runtime-proven shape requires a base array under schema.base |
| `slug` | body | `string` | no | Optional custom slug |
| `ttl_seconds` | body | `number` | no | Time to live in seconds for live context instances |
