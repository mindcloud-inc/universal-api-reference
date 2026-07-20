# Campfire: List Chart Transactions

Retrieves chart transactions from Campfire.

```
GET https://connect.mindcloud.co/v1/universal/campfire/latest/actions/list-chart-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campfire/latest/actions/list-chart-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campfire/latest/actions/list-chart-transactions?${params}`, {
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
      "count": 1,
      "is_truncated": true,
      "next": "string",
      "previous": "string",
      "results": [
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
| `count` | number |  |
| `is_truncated` | boolean |  |
| `next` | string |  |
| `previous` | string |  |
| `results` | array<object> |  |

## Native endpoint

Through the native Campfire API, this operation is `GET /coa/api/transaction` (base URL `https://api.meetcampfire.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chart-transactions.md) for the provider-specific parameters and requirements.

