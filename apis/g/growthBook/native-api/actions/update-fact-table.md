# Update a single fact table with GrowthBook

Updates an existing fact table in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/fact-tables/:id`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Update a single fact table](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the requested resource |
| `name` | body | `string` | no | — |
| `description` | body | `string` | no | Description of the fact table |
| `owner` | body | `string` | no | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. |
| `projects` | body | `list<string>` | no | List of associated project ids |
| `tags` | body | `list<string>` | no | List of associated tags |
| `userIdTypes` | body | `list<string>` | no | List of identifier columns in this table. For example, "id" or "anonymous_id" |
| `sql` | body | `string` | no | The SQL query for this fact table |
| `eventName` | body | `string` | no | The event name used in SQL template variables |
| `columns[]` | body | `array<object>` | no | Optional array of columns that you want to update. Only allows updating properties of existing columns. Cannot create new columns or delete existing ones. Columns cannot be added or deleted; column structure is determined by SQL parsing. Slice-related properties require an enterprise license. |
| `columns[]` | body | `array<object>` | no | Optional array of columns that you want to update. Only allows updating properties of existing columns. Cannot create new columns or delete existing ones. Columns cannot be added or deleted; column structure is determined by SQL parsing. Slice-related properties require an enterprise license. |
| `columnsError` | body | `string` | no | — |
| `managedBy` | body | `string` | no | Set this to "api" to disable editing in the GrowthBook UI |
| `archived` | body | `boolean` | no | — |
