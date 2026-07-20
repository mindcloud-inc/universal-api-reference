# Trint: Register Webhook Endpoint

Registers a webhook endpoint in Trint.

```
PUT https://connect.mindcloud.co/v1/universal/trint/latest/actions/register-webhook-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/trint/latest/actions/register-webhook-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trint/latest/actions/register-webhook-endpoint', {
  method: 'PUT',
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
      "callbackSubscriptions": [
        "string"
      ],
      "callbackUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callbackSubscriptions` | array<string> | Registered webhook event subscriptions. |
| `callbackUrl` | string | Registered webhook callback URL. |

## Native endpoint

Through the native Trint API, this operation is `PUT /callbacks/transcript/` (base URL `https://api.trint.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-webhook-endpoint.md) for the provider-specific parameters and requirements.

