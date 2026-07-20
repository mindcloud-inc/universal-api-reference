# QuickBooks Online: List Bills



```
GET https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-bills
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickBooks Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-bills?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-bills?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native QuickBooks Online API, this operation is `GET /query` (base URL `https://:quickbooksEnvironment/v3/company/:realmId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bills.md) for the provider-specific parameters and requirements.

