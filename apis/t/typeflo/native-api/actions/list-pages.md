# List Pages with Typeflo

Retrieves static site pages from Typeflo.

## Endpoint

- **Method:** `GET`
- **Path:** `/content/pages`
- **Base URL:** `https://{subdomain}.typeflo.io/api/headless`
- **Official documentation:** [List Pages](https://typeflo.io/knowledge-base/headless-cms-content-api-documentation)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | query | `string` | no | Filter pages by their unique slug. |
| `title` | query | `string` | no | Filter pages by title. |
| `is_draft` | query | `boolean` | no | Filter pages by draft status. |
