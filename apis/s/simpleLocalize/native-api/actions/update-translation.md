# Update Translation with SimpleLocalize

Updates a single translation in SimpleLocalize.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/translations`
- **Base URL:** `https://api.simplelocalize.io`
- **Official documentation:** [Update Translation](https://api.simplelocalize.io/openapi/ui#/Translations/updateTranslations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | body | `string` | yes | — |
| `language` | body | `string` | yes | — |
| `text` | body | `string` | yes | — |
| `customerId` | body | `string` | no | — |
| `namespace` | body | `string` | no | — |
| `reviewStatus` | body | `list` | no | Accepted values: ``, `NOT_REVIEWED`, `REVIEWED`. |
