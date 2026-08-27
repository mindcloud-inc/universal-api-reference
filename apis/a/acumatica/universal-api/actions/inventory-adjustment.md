# Acumatica: Inventory Adjustment



```
PUT https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/inventory-adjustment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/inventory-adjustment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/inventory-adjustment', {
  method: 'PUT',
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
| `Branch.value` | string | no |  |
| `BranchID.value` | string | no |  |
| `Date.value` | string | no |  |
| `Description.value` | string | no |  |
| `Details[].expirationDate.value` | string | no |  |
| `Details[].InventoryID` | object | no |  |
| `Details[].InventoryID.value` | string | no |  |
| `Details[].LocationID.value` | string | no |  |
| `Details[].LotSerialNbr.value` | string | no |  |
| `Details[].Qty.value` | number | no |  |
| `Details[].ReasonCode.value` | string | no |  |
| `Details[].UOM.value` | string | no |  |
| `Details[].UsrLogTranID.value` | string | no |  |
| `Details[].WarehouseID.value` | string | no |  |
| `ExternalRef.value` | string | no |  |
| `ReferenceNbr` | object | no |  |
| `ReferenceNbr.value` | string | no |  |
| `UsrLogAdjustment.value` | boolean | no |  |
| `Date` | object | no |  |
| `Details[].WarehouseID` | object | no |  |
| `Details[].LocationID` | object | no |  |
| `ExternalRef` | object | no |  |
| `Description` | object | no |  |
| `Details[].Qty` | object | no |  |
| `Branch` | object | no |  |
| `Details[].UOM` | object | no |  |
| `Details[]` | array | no |  |
| `Details[].LotSerialNbr` | object | no |  |
| `Details[].ReasonCode` | object | no |  |
| `UsrLogAdjustment` | object | no |  |
| `BranchID` | object | no |  |
| `Details[].expirationDate` | object | no |  |
| `Details[].UsrLogTranID` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Acumatica API returns.

## Native endpoint

Through the native Acumatica API, this operation is `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/InventoryAdjustment` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/inventory-adjustment.md) for the provider-specific parameters and requirements.

