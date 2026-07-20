# Nexiopay: View transaction async status



```
GET https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-transaction-async-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-transaction-async-status?connectionId=$CONNECTION_ID&asyncTraceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "asyncTraceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-transaction-async-status?${params}`, {
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
| `asyncTraceId` | string | yes | Async trace ID returned by the transaction request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asyncTraceId": "string",
      "id": "string",
      "message": "string",
      "status": "string",
      "transactionStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asyncTraceId` | string | Async trace ID. |
| `id` | string | Nexio payment ID. |
| `message` | string | Nexio response message. |
| `status` | string | Async request status. |
| `transactionStatus` | string | Transaction status. |

## Native endpoint

Through the native Nexiopay API, this operation is `GET /pay/v3/transactionAsyncStatus/{asyncTraceId}` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-transaction-async-status.md) for the provider-specific parameters and requirements.

