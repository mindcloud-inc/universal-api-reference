# QuickBooks Online: Create Bill



```
POST https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-bill
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickBooks Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-bill" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "vendorRef.value": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-bill', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "vendorRef.value": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `CheckPayment.BankAccountRef` | object | no |  |
| `CheckPayment.BankAccountRef.name` | string | no |  |
| `CurrencyRef.value` | string | no |  |
| `Line[].Amount` | number | no |  |
| `Line[].LinkedTxn[].TxnId` | string | no |  |
| `vendorRef` | object | no |  |
| `vendorRef.value` | string | yes | Vendor Id for the bill. Example: `1`. |
| `CheckPayment.BankAccountRef.value` | string | no |  |
| `Line[].LinkedTxn[]` | array | no |  |
| `Line[].LinkedTxn[].TxnType` | string | no | Default: `Bill`. |
| `TotalAmt` | number | no |  |
| `payType` | string | no |  |
| `PrivateNote` | string | no |  |
| `TxnDate` | string | no |  |
| `CurrencyRef` | object | no |  |
| `Line[]` | array | no |  |
| `CheckPayment` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": 1,
      "docNumber": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
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
| `balance` | number |  |
| `docNumber` | string |  |
| `dueDate` | date |  |
| `id` | string |  |
| `line` | array<object> |  |
| `metaData` | object |  |
| `syncToken` | string |  |
| `totalAmt` | number |  |
| `txnDate` | date |  |
| `vendorRef` | object |  |

## Native endpoint

Through the native QuickBooks Online API, this operation is `POST /billpayment` (base URL `https://:quickbooksEnvironment/v3/company/:realmId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bill.md) for the provider-specific parameters and requirements.

