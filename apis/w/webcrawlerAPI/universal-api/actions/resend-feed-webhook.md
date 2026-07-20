# Webcrawler API: Resend Feed Webhook

Resends a feed webhook from Webcrawler API.

```
PUT https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/resend-feed-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webcrawler API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/resend-feed-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/resend-feed-webhook', {
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
| `id` | string | yes | Feed identifier returned by List Feeds or Create Feed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "feed_run_id": "string",
      "items_sent": 1,
      "message": "string",
      "webhook_status": 1,
      "webhook_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `feed_run_id` | string | Feed run identifier that the webhook was resent for. |
| `items_sent` | number | Number of feed items included in the resent webhook. |
| `message` | string | Provider resend status message. |
| `webhook_status` | number | HTTP status code returned by the webhook receiver. |
| `webhook_url` | string | Webhook URL that received the resend attempt. |

## Native endpoint

Through the native Webcrawler API API, this operation is `POST /v2/feed/:id/webhook/resend` (base URL `https://api.webcrawlerapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resend-feed-webhook.md) for the provider-specific parameters and requirements.

