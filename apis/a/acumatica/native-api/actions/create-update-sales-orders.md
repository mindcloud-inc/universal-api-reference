# Create/Update Sales Orders with Acumatica

## Endpoint

- **Method:** `PUT`
- **Path:** `/entity/{endpointName}/{endpointVersion}/SalesOrder`
- **Base URL:** `{uRL}`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `OrderNbr` | body | `object` | no |
| `OrderType` | body | `object` | no |
| `CustomerID.value` | body | `string` | no |
| `customerOrder.value` | body | `string` | no |
| `Description.value` | body | `string` | no |
| `ExternalRef` | body | `object` | no |
| `ExternalRef.value` | body | `string` | no |
| `Hold.value` | body | `string` | no |
| `lastModified.value` | body | `string` | no |
| `OrderNbr.value` | body | `string` | no |
| `OrderType.value` | body | `string` | no |
| `preferredWarehouseID.value` | body | `string` | no |
| `requestedOn.value` | body | `string` | no |
| `Status.value` | body | `string` | no |
| `UsrLogShipID.value` | body | `string` | no |
| `UsrLogSyncDateTime.value` | body | `string` | no |
| `CustomerID` | body | `object` | no |
| `Status` | body | `object` | no |
| `Description` | body | `object` | no |
| `Hold` | body | `object` | no |
| `requestedOn` | body | `object` | no |
| `UsrLogShipID` | body | `object` | no |
| `preferredWarehouseID` | body | `object` | no |
| `customerOrder` | body | `object` | no |
| `UsrLogSyncDateTime` | body | `object` | no |
| `lastModified` | body | `object` | no |
