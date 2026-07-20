# Update Language with SimpleLocalize

Updates an existing language in SimpleLocalize.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/languages/{languageKey}`
- **Base URL:** `https://api.simplelocalize.io`
- **Official documentation:** [Update Language](https://api.simplelocalize.io/openapi/ui#/Languages/updateLanguage)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `languageKey` | path | `string` | yes |
| `key` | body | `string` | no |
| `name` | body | `string` | no |
