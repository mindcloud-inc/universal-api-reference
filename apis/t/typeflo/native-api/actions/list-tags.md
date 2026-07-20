# List Tags with Typeflo

Retrieves content tags from the Typeflo site.

## Endpoint

- **Method:** `GET`
- **Path:** `/content/tags`
- **Base URL:** `https://{subdomain}.typeflo.io/api/headless`
- **Official documentation:** [List Tags](https://typeflo.io/knowledge-base/headless-cms-content-api-documentation)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | query | `string` | no | Filter tags by their unique slug. |
| `name` | query | `string` | no | Filter tags by name. |
