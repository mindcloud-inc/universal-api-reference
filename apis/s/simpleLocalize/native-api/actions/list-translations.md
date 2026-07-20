# List Translations with SimpleLocalize

Retrieves translations from SimpleLocalize.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/translations`
- **Base URL:** `https://api.simplelocalize.io`
- **Official documentation:** [List Translations](https://api.simplelocalize.io/openapi/ui#/Translations/getTranslations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | query | `string` | no | — |
| `namespace` | query | `string` | no | — |
| `language` | query | `string` | no | — |
| `text` | query | `string` | no | — |
| `query` | query | `string` | no | — |
| `textStatus` | query | `list` | no | Accepted values: ``, `EMPTY`, `NOT_EMPTY`. |
| `customerId` | query | `string` | no | — |
| `baseOnly` | query | `boolean` | no | — |
| `reviewStatus` | query | `list` | no | Accepted values: ``, `NOT_REVIEWED`, `REVIEWED`. |
| `sortBy` | query | `list` | no | Accepted values: ``, `lastModifiedAt`. |
| `sortOrder` | query | `list` | no | Accepted values: `asc`, `desc`. |
| `version` | query | `list` | no | Accepted values: `REVIEWED`. |
