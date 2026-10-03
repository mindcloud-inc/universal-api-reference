# QuickBooks Online: List Accounts



```
GET https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickBooks Online `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0&query=select%20*%20from%20Account%20where%20AccountType%20%3D%20'Expense'" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query": "select * from Account where AccountType = 'Expense'"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-accounts?${params}`, {
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
| `query` | string | yes | QuickBooks SQL-like query. Add a WHERE clause to filter accounts, for example select * from Account where AccountType = 'Expense'. Default: `select * from Account`. Example: `select * from Account where AccountType = 'Expense'`. |

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

Through the native QuickBooks Online API, this operation is `GET /query` (base URL `https://:quickbooksEnvironment/v3/company/:realmId`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-accounts.md) for the provider-specific parameters and requirements.

