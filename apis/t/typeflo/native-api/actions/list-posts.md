# List Posts with Typeflo

Retrieves published blog posts from Typeflo.

## Endpoint

- **Method:** `GET`
- **Path:** `/content/posts`
- **Base URL:** `https://{subdomain}.typeflo.io/api/headless`
- **Official documentation:** [List Posts](https://typeflo.io/knowledge-base/headless-cms-content-api-documentation)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | query | `string` | no | Filter posts by their unique slug. |
| `author` | query | `string` | no | Filter posts by author ID. |
| `title` | query | `string` | no | Filter posts by title. |
| `toc_status` | query | `boolean` | no | Filter posts by table-of-contents status. |
| `restriction.status` | query | `boolean` | no | Filter posts by content restriction status. |
| `restriction.percentage` | query | `number` | no | Filter posts by restriction percentage. |
| `is_draft` | query | `boolean` | no | Filter posts by draft status. |
