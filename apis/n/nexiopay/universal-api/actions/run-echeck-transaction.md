# Nexiopay: Run echeck transaction



```
POST https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/run-echeck-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/run-echeck-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {},
  "tokenex": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/run-echeck-transaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {},
    "tokenex": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes | Transaction and customer data object documented by Nexio. |
| `tokenex` | object | yes | TokenEx payment token object documented by Nexio. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "currency": "string",
      "id": "string",
      "merchantId": "string",
      "message": "string",
      "transactionStatus": "string"
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
| `id` | string | Nexio payment ID. |
| `merchantId` | string | Nexio merchant ID. |
| `message` | string | Nexio response message. |
| `transactionStatus` | string | Transaction status. |

## Native endpoint

Through the native Nexiopay API, this operation is `POST /pay/v3/processECheck` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-echeck-transaction.md) for the provider-specific parameters and requirements.

