# Update Context with Rulebricks

Updates an existing context in Rulebricks.

## Endpoint

- **Method:** `PUT`
- **Path:** `/admin/contexts/:id`
- **Base URL:** `https://rulebricks.com/api/v1`
- **Official documentation:** [Update Context](https://rulebricks.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auto_execute_decisions` | body | `boolean` | no | Whether bound rules and flows auto-execute |
| `description` | body | `string` | no | Updated description of the context |
| `history_limit` | body | `number` | no | Maximum number of history entries to retain per field |
| `id` | path | `string` | yes | ID of the context to update |
| `name` | body | `string` | no | Updated name of the context |
| `on_schema_mismatch` | body | `string` | no | How to handle fields that do not match the schema |
| `schema` | body | `object<object>` | no | Context schema object. Runtime-proven shape requires a base array under schema.base |
| `slug` | body | `string` | no | Updated slug of the context |
| `ttl_seconds` | body | `number` | no | Time to live in seconds for live context instances |
