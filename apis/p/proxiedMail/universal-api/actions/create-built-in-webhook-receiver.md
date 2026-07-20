# ProxiedMail: Create Built-In Webhook Receiver



```
POST https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/create-built-in-webhook-receiver
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProxiedMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/create-built-in-webhook-receiver" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/create-built-in-webhook-receiver', {
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
      "callUrl": "https://example.com",
      "getUrl": "https://example.com",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callUrl` | string |  |
| `getUrl` | string |  |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native ProxiedMail API, this operation is `POST /callback` (base URL `https://proxiedmail.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-built-in-webhook-receiver.md) for the provider-specific parameters and requirements.

