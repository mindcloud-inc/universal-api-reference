# Get Visitor Inventory Item with Topia

Retrieves a specific visitor inventory item from Topia.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/world/:urlSlug/visitors/:visitorId/get-visitor-inventory-items/:itemId`
- **Base URL:** `https://api.topia.io/api`
- **Official documentation:** [Get Visitor Inventory Item](https://api.topia.io/api-docs/paths/v1/getVisitorSpecificInventoryItem.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urlSlug` | path | `string` | yes | Topia world URL slug. |
| `visitorId` | path | `string` | yes | Identifier for the visitor. |
| `itemId` | path | `string` | yes | Identifier for the inventory item. |
