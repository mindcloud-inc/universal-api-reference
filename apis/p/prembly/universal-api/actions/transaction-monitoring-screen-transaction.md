# Prembly: Transaction Monitoring Screen Transaction

Screens a transaction with Prembly monitoring.

```
POST https://connect.mindcloud.co/v1/universal/prembly/latest/actions/transaction-monitoring-screen-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/transaction-monitoring-screen-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prembly/latest/actions/transaction-monitoring-screen-transaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "currency": "string",
      "fraud_probability": 1,
      "geo_mismatch": true,
      "geo_mismatch_distance": 1,
      "id": "string",
      "internal_reference": "string",
      "ml_detection_reason": "string",
      "risk_level": "string",
      "risk_score": 1,
      "rules_triggered_count": 1,
      "status": "string",
      "transaction_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `currency` | string |  |
| `fraud_probability` | number |  |
| `geo_mismatch` | boolean |  |
| `geo_mismatch_distance` | number |  |
| `id` | string |  |
| `internal_reference` | string |  |
| `ml_detection_reason` | string |  |
| `risk_level` | string |  |
| `risk_score` | number |  |
| `rules_triggered_count` | number |  |
| `status` | string |  |
| `transaction_id` | string |  |

## Native endpoint

Through the native Prembly API, this operation is `POST /api/v1/fraud/transaction-monitoring/screen-transaction` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/transaction-monitoring-screen-transaction.md) for the provider-specific parameters and requirements.

