# Acumatica: Purchase Receipt



```
PUT https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/purchase-receipt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/purchase-receipt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/purchase-receipt', {
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
| `Date.value` | string | no |  |
| `Details[].ExpirationDate.value` | string | no |  |
| `Details[].LineNbr.value` | number | no |  |
| `Details[].Location.value` | string | no |  |
| `Details[].LotSerialNbr.value` | string | no |  |
| `Details[].Note.value` | string | no |  |
| `Details[].POLineNbr.value` | number | no |  |
| `Details[].POOrderNbr.value` | string | no |  |
| `Details[].POOrderType.value` | string | no |  |
| `Details[].ReceiptQty` | object | no |  |
| `Details[].ReceiptQty.value` | number | no |  |
| `Details[].UsrLogTranID.value` | string | no |  |
| `Details[].UsrLPNbr.value` | string | no |  |
| `expand` | string | no |  |
| `Hold.value` | boolean | no |  |
| `Location.value` | string | no |  |
| `Note.value` | string | no |  |
| `ReceiptNbr.value` | string | no |  |
| `Type.value` | string | no |  |
| `UsrLogReceiptID.value` | string | no |  |
| `UsrLogReceived.value` | boolean | no |  |
| `VendorID.value` | string | no |  |
| `Details[].POOrderType` | object | no |  |
| `Type` | object | no |  |
| `Details[].POOrderNbr` | object | no |  |
| `Hold` | object | no |  |
| `Date` | object | no |  |
| `Details[].POLineNbr` | object | no |  |
| `Details[].LotSerialNbr` | object | no |  |
| `VendorID` | object | no |  |
| `Details[].ExpirationDate` | object | no |  |
| `Location` | object | no |  |
| `Branch` | object | no |  |
| `Details[].UsrLPNbr` | object | no |  |
| `Details[].UsrLogTranID` | object | no |  |
| `Note` | object | no |  |
| `Details[]` | array | no |  |
| `Details[].Note` | object | no |  |
| `Details[].Location` | object | no |  |
| `UsrLogReceived` | object | no |  |
| `Details[].LineNbr` | object | no |  |
| `ReceiptNbr` | object | no |  |
| `UsrLogReceiptID` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Acumatica API returns.

## Native endpoint

Through the native Acumatica API, this operation is `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/PurchaseReceipt` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/purchase-receipt.md) for the provider-specific parameters and requirements.

