# List Translation Keys With Metadata with SimpleLocalize

Retrieves translation keys with metadata from SimpleLocalize.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/translation-keys`
- **Base URL:** `https://api.simplelocalize.io`
- **Official documentation:** [List Translation Keys With Metadata](https://api.simplelocalize.io/openapi/ui#/Translation%20keys/getTranslationKeys)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | query | `string` | no | — |
| `namespace` | query | `string` | no | — |
| `sort` | query | `list` | no | Accepted values: `created_at`, `deprecated_at`, `last_seen_at`, `modified_at`. |
