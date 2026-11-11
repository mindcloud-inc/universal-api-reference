# Get Sales Order with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `GET`
- **Path:** `v2.0/companies(:companyId)/salesOrders(:salesOrderId)`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST
- **Official documentation:** [Get Sales Order](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_salesorder_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `list<string>` | yes | The Business Central company that holds the sales order. |
| `salesOrderId` | path | `string` | yes | The sales order's system ID (GUID), not the order number. |
