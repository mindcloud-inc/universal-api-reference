# QuickBooks Online: Get Invoice



```
GET https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickBooks Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/get-invoice?connectionId=$CONNECTION_ID&invoiceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoiceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/get-invoice?${params}`, {
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
| `invoiceId` | string | yes | QuickBooks Invoice Id. |

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

Through the native QuickBooks Online API, this operation is `GET /invoice/:invoiceId` (base URL `https://:quickbooksEnvironment/v3/company/:realmId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

