# Update Contact Lifecycle with respond.io

Updates a contact lifecycle in respond.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/:identifier/lifecycle/update`
- **Base URL:** `https://api.respond.io/v2`
- **Official documentation:** [Update Contact Lifecycle](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/contact-api.yml/paths/~1contact~1%7Bidentifier%7D~1lifecycle~1update/post?fromExportButton=true&snapshotType=http_operation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Contact identifier (id:, email:, or phone:). |
| `name` | body | `string` | yes | Lifecycle name to apply. |
