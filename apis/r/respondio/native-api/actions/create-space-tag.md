# Create Space Tag with respond.io

Creates a new space tag in respond.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/space/tag`
- **Base URL:** `https://api.respond.io/v2`
- **Official documentation:** [Create Space Tag](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/space-api.yml/paths/~1space~1tag/post?fromExportButton=true&snapshotType=http_operation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `colorCode` | body | `string` | no | Hex color code for the tag. |
| `description` | body | `string` | no | Space tag description. |
| `emoji` | body | `string` | no | Emoji for the tag. |
| `name` | body | `string` | yes | Space tag name. |
