# Delete Tags with respond.io

Deletes tags from a contact in respond.io.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contact/:identifier/tag`
- **Base URL:** `https://api.respond.io/v2`
- **Official documentation:** [Delete Tags](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/contact-api.yml/paths/~1contact~1%7Bidentifier%7D~1tag/delete?fromExportButton=true&snapshotType=http_operation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Contact identifier (id:, email:, or phone:). |
| `identify` | query | `string` | no | Tag identifier to delete. |
| `tags` | body | `string` | yes | Tag(s) to remove. |
