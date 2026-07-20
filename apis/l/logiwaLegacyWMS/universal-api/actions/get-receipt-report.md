# Logiwa Legacy WMS: Get Receipt Report

By using this endpoint, the users can obtain the receipt records.

```
POST https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/get-receipt-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logiwa Legacy WMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/get-receipt-report" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/get-receipt-report', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `InventorySiteID` | string | no | ID of inventory site. |
| `WarehouseID` | string | no | Id of the warehouse that receives receipt order |
| `DepositorID` | string | no | Id of depositor (client) who owns the inventory item to be received |
| `WarehouseReceiptID` | string | no | Id of receipt if the receipt order is received. ( Use List Receipt Orders to obtain this value ) |
| `InventoryItemID` | string | no | Id of inventory item received or will be received. ( Use Get Item ID ) |
| `ReferanceNo` | string | no | Reference number |
| `IsReturn` | boolean | no | If yes, the receive order is created for return operation. |
| `ReceiptDateTimeStart` | date | no | ReceiptDateTime_Start |
| `ReceiptDateTime_End` | date | no | ReceiptDateTime_End |
| `freeAttr3` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Logiwa Legacy WMS API returns.

## Native endpoint

Through the native Logiwa Legacy WMS API, this operation is `POST en/api/IntegrationApi/ReceiptAllSearch` (base URL `https://{{credentials.uRL}}.logiwa.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-receipt-report.md) for the provider-specific parameters and requirements.

