# Delete Contact with respond.io

Deletes a contact from respond.io.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contact/:identifier`
- **Base URL:** `https://api.respond.io/v2`
- **Official documentation:** [Delete Contact](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/contact-api.yml/paths/~1contact~1%7Bidentifier%7D/delete?fromExportButton=true&snapshotType=http_operation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Contact identifier (id:, email:, or phone:). |
