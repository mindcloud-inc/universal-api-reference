# ProxiedMail: Get Built-In Webhook Receiver Payload



```
GET https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/get-built-in-webhook-receiver-payload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProxiedMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/get-built-in-webhook-receiver-payload?connectionId=$CONNECTION_ID&hash=589cd2f2feb8c6eac279e778392ec873" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hash": "589cd2f2feb8c6eac279e778392ec873"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/get-built-in-webhook-receiver-payload?${params}`, {
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
| `hash` | string | yes | Example: `589cd2f2feb8c6eac279e778392ec873`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "isReceived": true,
      "method": "string",
      "payload": {
        "kind": "string",
        "source": "string",
        "timestamp": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `isReceived` | boolean |  |
| `method` | string |  |
| `payload.kind` | string |  |
| `payload.source` | string |  |
| `payload.timestamp` | string |  |
| `status` | string |  |

## Native endpoint

Through the native ProxiedMail API, this operation is `GET /callback/get/:hash` (base URL `https://proxiedmail.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-built-in-webhook-receiver-payload.md) for the provider-specific parameters and requirements.

