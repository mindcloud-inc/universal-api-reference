# Activate Inventory Item with Shopify

Activates an inventory item in Shopify.

## Endpoint

- **Method:** `POST`
- **Path:** `/:apiVersion/graphql.json`
- **Base URL:** `https://{storeName}.myshopify.com/admin/api/`
- **API:** GraphQL
- **Official documentation:** [Activate Inventory Item](https://shopify.dev/docs/api/admin-graphql/latest/mutations/inventoryActivate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `apiVersion` | path | `string` | no | e.g. `2026-01`  As of version 2026-01, this mutation supports an optional idempotency key using the @idempotent directive. As of version 2026-04, the idempotency key is required and must be provided using the @idempotent directive. For more information, see the idempotency documentation. |
| `variables` | body | `object` | no | — |
| `variables.inventoryItemId` | body | `string` | yes | The ID of the location of the inventory item being activated. |
| `query` | body | `string` | no | This mutation __Activates an inventory item at a location with idempotency enabled__  To see all available examples [see the documentation](https://shopify.dev/docs/api/admin-graphql/latest/mutations/inventoryActivate?example=activate-an-inventory-item-at-a-location-with-idempotency-enabled-2026-01-onwards) |
| `variables.locationId` | body | `string` | yes | The ID of the location of the inventory item being activated. |
