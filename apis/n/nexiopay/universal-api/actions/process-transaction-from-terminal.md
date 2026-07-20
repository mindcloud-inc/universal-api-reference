# Nexiopay: Process transaction from terminal



```
POST https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/process-transaction-from-terminal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/process-transaction-from-terminal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "terminalId": "string",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/process-transaction-from-terminal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "terminalId": "string",
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `terminalId` | string | yes | Terminal ID returned by the terminal list endpoint. |
| `data` | object | yes | Retail transaction and customer data object documented by Nexio. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "currency": "string",
      "id": "string",
      "status": "string",
      "terminalRequestId": "string"
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
| `status` | string | Terminal transaction status. |
| `terminalRequestId` | string | Terminal request ID. |

## Native endpoint

Through the native Nexiopay API, this operation is `POST /pay/v3/processFromTerminal` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/process-transaction-from-terminal.md) for the provider-specific parameters and requirements.

