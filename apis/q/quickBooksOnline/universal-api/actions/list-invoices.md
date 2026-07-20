# QuickBooks Online: List Invoices



```
GET https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickBooks Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-invoices?connectionId=$CONNECTION_ID&query=select%20*%20from%20Invoice%20where%20Metadata.LastUpdatedTime%20%3E%20'2025-01-14T00%3A00%3A00.000Z'%20order%20by%20Metadata.LastUpdatedTime%20DESC" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "select * from Invoice where Metadata.LastUpdatedTime > '2025-01-14T00:00:00.000Z' order by Metadata.LastUpdatedTime DESC"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-invoices?${params}`, {
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
| `query` | string | yes | Fixed query used to list invoices. Default: `select * from Invoice where Metadata.LastUpdatedTime > '2025-01-14T00:00:00.000Z' order by Metadata.LastUpdatedTime DESC`. |

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

Through the native QuickBooks Online API, this operation is `GET /query` (base URL `https://:quickbooksEnvironment/v3/company/:realmId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

