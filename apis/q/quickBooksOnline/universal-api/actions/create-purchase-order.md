# QuickBooks Online: Create Purchase Order



```
POST https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickBooks Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-purchase-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "vendorRef.value": "1",
  "Line[0].Amount": 1,
  "Line[0].AccountBasedExpenseLineDetail.AccountRef.value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-purchase-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "vendorRef.value": "1",
    "Line[0].Amount": 1,
    "Line[0].AccountBasedExpenseLineDetail.AccountRef.value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `vendorRef.value` | string | yes | Vendor Id for the purchase order. Example: `1`. |
| `Line[0].Amount` | number | yes | Amount for the first purchase order expense line. |
| `Line[0].AccountBasedExpenseLineDetail.AccountRef.value` | string | yes | Expense account ID for the first purchase order line. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "docNumber": "string",
      "id": "string",
      "line": [
        {}
      ],
      "metaData": {},
      "syncToken": "string",
      "totalAmt": 1,
      "txnDate": "2026-05-07T12:00:00.000Z",
      "vendorRef": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `docNumber` | string |  |
| `id` | string |  |
| `line` | array<object> |  |
| `metaData` | object |  |
| `syncToken` | string |  |
| `totalAmt` | number |  |
| `txnDate` | date |  |
| `vendorRef` | object |  |

## Native endpoint

Through the native QuickBooks Online API, this operation is `POST /purchaseorder` (base URL `https://:quickbooksEnvironment/v3/company/:realmId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-purchase-order.md) for the provider-specific parameters and requirements.

