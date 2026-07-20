# List Tiers with Ghost

Retrieves tiers from Ghost.

## Endpoint

- **Method:** `GET`
- **Path:** `/tiers/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [List Tiers](https://docs.ghost.org/admin-api/tiers/overview)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include` | query | `string` | no | Comma-separated related tier resources to include, such as monthly_price, yearly_price, or benefits. |
| `filter` | query | `string` | no | Ghost filter expression for narrowing tiers by type, visibility, or active status. |
