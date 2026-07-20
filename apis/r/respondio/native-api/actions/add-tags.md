# Add Tags with respond.io

Adds tags to a contact in respond.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/:identifier/tag`
- **Base URL:** `https://api.respond.io/v2`
- **Official documentation:** [Add Tags](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/contact-api.yml/paths/~1contact~1%7Bidentifier%7D~1tag/post?fromExportButton=true&snapshotType=http_operation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Contact identifier (id:, email:, or phone:). |
| `tags` | body | `string` | yes | Tag(s) to add. |
