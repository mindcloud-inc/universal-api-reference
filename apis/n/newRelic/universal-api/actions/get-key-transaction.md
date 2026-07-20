# New Relic: Get Key Transaction

Retrieves a key transaction from New Relic.

```
GET https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/get-key-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a New Relic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/get-key-transaction?connectionId=$CONNECTION_ID&keyTransactionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keyTransactionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/get-key-transaction?${params}`, {
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
| `keyTransactionId` | number | yes | New Relic key transaction ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "key_transaction": {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key_transaction.application_summary.apdex_score` | number |  |
| `key_transaction.application_summary.apdex_target` | number |  |
| `key_transaction.application_summary.error_rate` | number |  |
| `key_transaction.application_summary.response_time` | number |  |
| `key_transaction.application_summary.throughput` | number |  |
| `key_transaction.id` | number |  |
| `key_transaction.links.application` | number |  |
| `key_transaction.name` | string |  |
| `key_transaction.transaction_name` | string |  |

## Native endpoint

Through the native New Relic API, this operation is `GET /key_transactions/:keyTransactionId.json` (base URL `https://api.newrelic.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-key-transaction.md) for the provider-specific parameters and requirements.

