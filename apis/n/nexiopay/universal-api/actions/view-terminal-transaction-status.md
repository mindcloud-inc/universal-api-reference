# Nexiopay: View terminal transaction status



```
GET https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-terminal-transaction-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-terminal-transaction-status?connectionId=$CONNECTION_ID&terminalRequestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "terminalRequestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-terminal-transaction-status?${params}`, {
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
| `terminalRequestId` | string | yes | Terminal request ID returned by a terminal transaction request. |

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

Through the native Nexiopay API, this operation is `GET /pay/v3/processFromTerminal/{terminalRequestId}` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-terminal-transaction-status.md) for the provider-specific parameters and requirements.

