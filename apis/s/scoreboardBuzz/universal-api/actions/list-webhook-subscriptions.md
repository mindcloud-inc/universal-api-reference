# Scoreboard Buzz: List Webhook Subscriptions

Retrieves webhook subscriptions from Scoreboard Buzz.

```
GET https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/list-webhook-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoreboard Buzz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/list-webhook-subscriptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/list-webhook-subscriptions?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "event_type": "string",
      "id": 1,
      "status": 1,
      "target_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | Creation timestamp. |
| `event_type` | string | Subscribed webhook event type. |
| `id` | number | Webhook subscription ID. |
| `status` | number | Provider status code for the subscription. |
| `target_url` | string | Webhook callback URL that will receive deliveries. |

## Native endpoint

Through the native Scoreboard Buzz API, this operation is `GET /webhooks/subscriptions` (base URL `https://api.scoreboardbuzz.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-subscriptions.md) for the provider-specific parameters and requirements.

