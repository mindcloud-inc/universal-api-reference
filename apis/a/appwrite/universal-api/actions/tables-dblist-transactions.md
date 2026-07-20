# Appwrite: List transactions

Retrieves a list of transactions from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dblist-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dblist-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dblist-transactions?${params}`, {
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
| `queries[]` | array<string> | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "total": 1,
      "transactions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `total` | number | Total number of transactions that matched your query. |
| `transactions` | array<object> | List of transactions. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /tablesdb/transactions` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/tables-dblist-transactions.md) for the provider-specific parameters and requirements.

