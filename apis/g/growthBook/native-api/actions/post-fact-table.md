# Create a single fact table with GrowthBook

Creates a new fact table in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/fact-tables`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Create a single fact table](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `description` | body | `string` | no | Description of the fact table |
| `owner` | body | `string` | no | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. |
| `projects` | body | `list<string>` | no | List of associated project ids |
| `tags` | body | `list<string>` | no | List of associated tags |
| `datasource` | body | `string` | yes | The datasource id |
| `userIdTypes` | body | `list<string>` | yes | List of identifier columns in this table. For example, "id" or "anonymous_id" |
| `sql` | body | `string` | yes | The SQL query for this fact table |
| `eventName` | body | `string` | no | The event name used in SQL template variables |
| `managedBy` | body | `string` | no | Set this to "api" to disable editing in the GrowthBook UI |
