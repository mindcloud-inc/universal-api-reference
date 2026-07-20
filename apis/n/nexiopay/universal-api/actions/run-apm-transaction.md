# Nexiopay: Run APM transaction



```
POST https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/run-apm-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/run-apm-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "apm": {},
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/run-apm-transaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "apm": {},
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `apm` | object | yes | Alternative payment method token object documented by Nexio. |
| `data` | object | yes | APM transaction data object documented by Nexio. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "currency": "string",
      "id": "string",
      "message": "string",
      "paymentMethod": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Transaction amount. |
| `currency` | string | Transaction currency. |
| `id` | string | Nexio APM payment ID. |
| `message` | string | Nexio response message. |
| `paymentMethod` | string | APM payment method. |
| `status` | string | APM transaction status. |

## Native endpoint

Through the native Nexiopay API, this operation is `POST /apm/v3/process` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-apm-transaction.md) for the provider-specific parameters and requirements.

