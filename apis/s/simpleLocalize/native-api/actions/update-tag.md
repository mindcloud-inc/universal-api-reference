# Update Tag with SimpleLocalize

Updates an existing tag in SimpleLocalize.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/tags/{tagName}`
- **Base URL:** `https://api.simplelocalize.io`
- **Official documentation:** [Update Tag](https://api.simplelocalize.io/openapi/ui#/Tags/updateTag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tagName` | path | `string` | yes | — |
| `name` | body | `string` | no | Tag name |
| `color` | body | `string` | no | Tag color |
