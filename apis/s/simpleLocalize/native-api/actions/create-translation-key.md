# Create Translation Key with SimpleLocalize

Creates a new translation key in SimpleLocalize.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/translation-keys`
- **Base URL:** `https://api.simplelocalize.io`
- **Official documentation:** [Create Translation Key](https://api.simplelocalize.io/openapi/ui#/Translation%20keys/createTranslationKey)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `key` | body | `string` | yes |
| `namespace` | body | `string` | no |
| `description` | body | `string` | no |
| `codeDescription` | body | `string` | no |
| `charactersLimit` | body | `number` | no |
| `lock` | body | `boolean` | no |
| `deprecated` | body | `boolean` | no |
| `tags[]` | body | `array<string>` | no |
