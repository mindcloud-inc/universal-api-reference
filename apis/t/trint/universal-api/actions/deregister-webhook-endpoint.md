# Trint: Deregister Webhook Endpoint

Deregisters a webhook endpoint from Trint.

```
DELETE https://connect.mindcloud.co/v1/universal/trint/latest/actions/deregister-webhook-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/trint/latest/actions/deregister-webhook-endpoint?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trint/latest/actions/deregister-webhook-endpoint?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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
| `callbackSubscriptions` | array<string> | Webhook event subscriptions removed for the callback. |
| `callbackUrl` | string | Deregistered webhook callback URL. |

## Native endpoint

Through the native Trint API, this operation is `DELETE /callbacks/transcript/` (base URL `https://api.trint.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/deregister-webhook-endpoint.md) for the provider-specific parameters and requirements.

