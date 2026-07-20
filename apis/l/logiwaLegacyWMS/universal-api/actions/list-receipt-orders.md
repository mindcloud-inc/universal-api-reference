# Logiwa Legacy WMS: List Receipt Orders



```
GET https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-receipt-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logiwa Legacy WMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-receipt-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-receipt-orders?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `iD` | number | no |  |
| `Code` | string | no |  |
| `WarehouseID` | number | no |  |
| `DepositorID` | number | no |  |
| `inventorySiteID` | number | no |  |
| `purchaseOrderID` | string | no |  |
| `InventorySiteDescription` | string | no |  |
| `IsGetOrderDetails` | boolean | no |  |
| `IntegrationKey` | string | no |  |
| `WarehouseReceiptTypeDescription` | string | no |  |
| `warehouseReceiptStatusID[]` | array<number> | no |  |
| `warehouseReceiptStatusDescription` | string | no |  |
| `warehouseReceiptTypeID` | string | no |  |
| `warehouseReceiptTypeDescription` | string | no | The `WarehouseReceiptTypeDescription` Example 'Return' |
| `receiptDate` | date | no |  |
| `receiptDateStart` | date | no |  |
| `receiptDate_End` | date | no |  |
| `actualArrivalDate` | date | no |  |
| `actualArrivalDateStart` | date | no |  |
| `actualArrivalDateEnd` | date | no |  |
| `lastModifiedDate` | date | no |  |
| `lastModifiedDateStart` | date | no |  |
| `lastModifiedDateEnd` | date | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Logiwa Legacy WMS API returns.

## Native endpoint

Through the native Logiwa Legacy WMS API, this operation is `POST en/api/IntegrationApi/WarehouseReceiptSearch` (base URL `https://{{credentials.uRL}}.logiwa.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-receipt-orders.md) for the provider-specific parameters and requirements.

