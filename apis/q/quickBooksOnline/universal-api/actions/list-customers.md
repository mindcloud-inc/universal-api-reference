# QuickBooks Online: List Customers



```
GET https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickBooks Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-customers?${params}`, {
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
      "active": true,
      "balance": 1,
      "companyName": "Ava Chen",
      "currencyRef": {},
      "displayName": "Ava Chen",
      "fullyQualifiedName": "Ava Chen",
      "id": "string",
      "metaData": {},
      "primaryEmailAddr": {},
      "syncToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `balance` | number |  |
| `companyName` | string |  |
| `currencyRef` | object |  |
| `displayName` | string |  |
| `fullyQualifiedName` | string |  |
| `id` | string |  |
| `metaData` | object |  |
| `primaryEmailAddr` | object |  |
| `syncToken` | string |  |

## Native endpoint

Through the native QuickBooks Online API, this operation is `GET /query` (base URL `https://:quickbooksEnvironment/v3/company/:realmId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

