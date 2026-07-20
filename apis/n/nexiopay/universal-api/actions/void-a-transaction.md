# Nexiopay: Void a transaction



```
PUT https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/void-a-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/void-a-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/void-a-transaction', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Nexio payment ID to void. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `currency` | string | Transaction currency. |
| `id` | string | Nexio payment ID. |
| `merchantId` | string | Nexio merchant ID. |
| `message` | string | Nexio response message. |
| `transactionStatus` | string | Void transaction status. |

## Native endpoint

Through the native Nexiopay API, this operation is `POST /pay/v3/void` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/void-a-transaction.md) for the provider-specific parameters and requirements.

