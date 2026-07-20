# Update Translation Key with SimpleLocalize

Updates an existing translation key in SimpleLocalize.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/translation-keys`
- **Base URL:** `https://api.simplelocalize.io`
- **Official documentation:** [Update Translation Key](https://api.simplelocalize.io/openapi/ui#/Translation%20keys/updateTranslationKey)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `key` | query | `string` | yes |
| `namespace` | query | `string` | no |
| `key` | body | `string` | no |
| `namespace` | body | `string` | no |
| `description` | body | `string` | no |
| `codeDescription` | body | `string` | no |
| `charactersLimit` | body | `number` | no |
| `deprecated` | body | `boolean` | no |
| `lock` | body | `boolean` | no |
| `tags[]` | body | `array<string>` | no |
