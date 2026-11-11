# List Purchase Orders with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `GET`
- **Path:** `v2.0/companies(:companyId)/purchaseOrders`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST
- **Official documentation:** [List Purchase Orders](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/resources/dynamics_purchaseorder)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | Optional OData filter on purchase order fields, such as number, vendorNumber, status or lastModifiedDateTime. Example: vendorNumber eq '20000' and totalAmountIncludingTax gt 1000 |
| `companyId` | path | `list<string>` | yes | The Business Central company that holds the purchase orders. |
