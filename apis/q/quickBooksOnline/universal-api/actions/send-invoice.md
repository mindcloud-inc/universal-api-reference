# QuickBooks Online: Send Invoice



```
PUT https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/send-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickBooks Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/send-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/send-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceId` | string | yes | QuickBooks Invoice Id to send. |
| `sendTo` | string | no | Optional recipient email for QuickBooks invoice send. If omitted, QuickBooks uses the invoice/customer email on file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": 1,
      "customerRef": {},
      "docNumber": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "emailStatus": "ava@example.com",
      "id": "string",
      "line": [
        {}
      ],
      "metaData": {},
      "syncToken": "string",
      "totalAmt": 1,
      "txnDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number |  |
| `customerRef` | object |  |
| `docNumber` | string |  |
| `dueDate` | date |  |
| `emailStatus` | string |  |
| `id` | string |  |
| `line` | array<object> |  |
| `metaData` | object |  |
| `syncToken` | string |  |
| `totalAmt` | number |  |
| `txnDate` | date |  |

## Native endpoint

Through the native QuickBooks Online API, this operation is `POST /invoice/:invoiceId/send` (base URL `https://:quickbooksEnvironment/v3/company/:realmId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-invoice.md) for the provider-specific parameters and requirements.

