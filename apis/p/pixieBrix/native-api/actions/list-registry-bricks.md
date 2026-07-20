# List Registry Bricks with PixieBrix

Retrieves brick packages from the PixieBrix registry.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/registry/bricks/`
- **Base URL:** `https://app.pixiebrix.com`
- **Official documentation:** [List Registry Bricks](https://docs.pixiebrix.com/developer-api/package-management-apis)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `kind` | query | `string` | no | Registry brick kind filter. |
| `kind__in` | query | `string` | no | Comma-separated registry brick kinds to include. |
