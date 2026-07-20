# Update Space Tag with respond.io

Updates an existing space tag in respond.io.

## Endpoint

- **Method:** `PUT`
- **Path:** `/space/tag`
- **Base URL:** `https://api.respond.io/v2`
- **Official documentation:** [Update Space Tag](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/space-api.yml/paths/~1space~1tag/put?fromExportButton=true&snapshotType=http_operation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `colorCode` | body | `string` | no | Hex color code for the tag. |
| `currentName` | body | `string` | yes | Current space tag name. |
| `description` | body | `string` | no | Space tag description. |
| `emoji` | body | `string` | no | Emoji for the tag. |
| `name` | body | `string` | no | New space tag name. |
