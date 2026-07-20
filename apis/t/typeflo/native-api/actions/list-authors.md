# List Authors with Typeflo

Retrieves author profiles from the Typeflo site.

## Endpoint

- **Method:** `GET`
- **Path:** `/content/authors`
- **Base URL:** `https://{subdomain}.typeflo.io/api/headless`
- **Official documentation:** [List Authors](https://typeflo.io/knowledge-base/headless-cms-content-api-documentation)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | query | `string` | no | Filter authors by their unique slug. |
| `name` | query | `string` | no | Filter authors by name. |
| `email` | query | `string` | no | Filter authors by email address. |
