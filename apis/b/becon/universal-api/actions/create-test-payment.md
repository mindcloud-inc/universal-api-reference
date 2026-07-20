# Becon: Create Test Payment

Creates a test payment in Becon.

```
POST https://connect.mindcloud.co/v1/universal/becon/latest/actions/create-test-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Becon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/becon/latest/actions/create-test-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "currency_id": "string",
  "store_id": "string",
  "sum": "string",
  "transaction_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/becon/latest/actions/create-test-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "currency_id": "string",
    "store_id": "string",
    "sum": "string",
    "transaction_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | no | Output address when simulating a BTC store payment. |
| `currency_id` | string | yes | Currency id to simulate. |
| `memo` | string | no | Memo when simulating a BNB store payment. |
| `store_id` | string | yes | Target store id to simulate. |
| `sum` | string | yes | Payment amount to simulate. |
| `transaction_id` | string | yes | Test blockchain transaction id string. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider confirmation message for the test payment. |

## Native endpoint

Through the native Becon API, this operation is `POST /v1/test` (base URL `https://external-api.bcon.global/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-test-payment.md) for the provider-specific parameters and requirements.

