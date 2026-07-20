# Timeular: List Webhook Subscriptions

Retrieves webhook subscriptions from your Timeular workspace.

```
GET https://connect.mindcloud.co/v1/universal/timeular/latest/actions/list-webhook-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/list-webhook-subscriptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeular/latest/actions/list-webhook-subscriptions?${params}`, {
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
      "subscriptions": [
        {
          "event": "string",
          "id": "string",
          "targetUrl": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `subscriptions[].event` | string |  |
| `subscriptions[].id` | string |  |
| `subscriptions[].targetUrl` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `GET /api/v4/webhooks/subscription` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-subscriptions.md) for the provider-specific parameters and requirements.

