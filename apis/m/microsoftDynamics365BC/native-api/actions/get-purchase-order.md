# Get Purchase Order with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `GET`
- **Path:** `v2.0/companies(:companyId)/purchaseOrders(:purchaseOrderId)`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST
- **Official documentation:** [Get Purchase Order](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_purchaseorder_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `list<string>` | yes | The Business Central company that holds the purchase order. |
| `purchaseOrderId` | path | `string` | yes | The purchase order's system ID (GUID), not the order number. |
