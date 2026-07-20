# Update Translation Key by ID with SimpleLocalize

Updates an existing translation key by ID in SimpleLocalize.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/translation-keys/{id}`
- **Base URL:** `https://api.simplelocalize.io`
- **Official documentation:** [Update Translation Key by ID](https://api.simplelocalize.io/openapi/ui#/Translation%20keys/updateTranslationKeyById)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `key` | body | `string` | no |
| `namespace` | body | `string` | no |
| `description` | body | `string` | no |
| `codeDescription` | body | `string` | no |
| `charactersLimit` | body | `number` | no |
| `deprecated` | body | `boolean` | no |
| `lock` | body | `boolean` | no |
| `tags[]` | body | `array<string>` | no |
