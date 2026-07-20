# QuickBooks Online: Create Invoice



```
POST https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickBooks Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerRef.value": "1",
  "Line[0].Amount": 1,
  "Line[0].SalesItemLineDetail.ItemRef.value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerRef.value": "1",
    "Line[0].Amount": 1,
    "Line[0].SalesItemLineDetail.ItemRef.value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerRef.value` | string | yes | Customer Id for the invoice. Example: `1`. |
| `Line[0].Amount` | number | yes | Amount for the first invoice line item. |
| `Line[0].SalesItemLineDetail.ItemRef.value` | string | yes | Item ID to bill on the first invoice line. |

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

Through the native QuickBooks Online API, this operation is `POST /invoice` (base URL `https://:quickbooksEnvironment/v3/company/:realmId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

