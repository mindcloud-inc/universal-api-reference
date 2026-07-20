# List Visitor Inventory Items with Topia

Retrieves a visitor's inventory items from Topia.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/world/:urlSlug/visitors/:visitorId/get-visitor-inventory-items`
- **Base URL:** `https://api.topia.io/api`
- **Official documentation:** [List Visitor Inventory Items](https://api.topia.io/api-docs/paths/v1/getVisitorInventoryItems.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urlSlug` | path | `string` | yes | Topia world URL slug. |
| `visitorId` | path | `string` | yes | Identifier for the visitor. |
