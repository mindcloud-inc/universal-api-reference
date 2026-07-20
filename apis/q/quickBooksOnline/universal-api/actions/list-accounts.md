# QuickBooks Online: List Accounts



```
GET https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickBooks Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-accounts?${params}`, {
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
      "accountSubType": "string",
      "accountType": "string",
      "active": true,
      "classification": "string",
      "currentBalance": 1,
      "fullyQualifiedName": "Ava Chen",
      "id": "string",
      "metaData": {},
      "name": "Ava Chen",
      "syncToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountSubType` | string |  |
| `accountType` | string |  |
| `active` | boolean |  |
| `classification` | string |  |
| `currentBalance` | number |  |
| `fullyQualifiedName` | string |  |
| `id` | string |  |
| `metaData` | object |  |
| `name` | string |  |
| `syncToken` | string |  |

## Native endpoint

Through the native QuickBooks Online API, this operation is `GET /query` (base URL `https://:quickbooksEnvironment/v3/company/:realmId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-accounts.md) for the provider-specific parameters and requirements.

