# New Relic: List Key Transactions

Retrieves key transactions from New Relic.

```
GET https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-key-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a New Relic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-key-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-key-transactions?${params}`, {
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
      "key_transactions": [
        {
          "application_summary": {
            "apdex_score": 1,
            "apdex_target": 1,
            "error_rate": 1,
            "response_time": 1,
            "throughput": 1
          },
          "id": 1,
          "links": {
            "application": 1
          },
          "name": "Ava Chen",
          "transaction_name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key_transactions[].application_summary.apdex_score` | number |  |
| `key_transactions[].application_summary.apdex_target` | number |  |
| `key_transactions[].application_summary.error_rate` | number |  |
| `key_transactions[].application_summary.response_time` | number |  |
| `key_transactions[].application_summary.throughput` | number |  |
| `key_transactions[].id` | number |  |
| `key_transactions[].links.application` | number |  |
| `key_transactions[].name` | string |  |
| `key_transactions[].transaction_name` | string |  |

## Native endpoint

Through the native New Relic API, this operation is `GET /key_transactions.json` (base URL `https://api.newrelic.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-key-transactions.md) for the provider-specific parameters and requirements.

