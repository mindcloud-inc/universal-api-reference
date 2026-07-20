# Drag'n Survey: Subscribe to Webhook

Creates a webhook subscription in Drag'n Survey.

```
POST https://connect.mindcloud.co/v1/universal/dragnSurvey/latest/actions/subscribe-to-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Drag'n Survey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dragnSurvey/latest/actions/subscribe-to-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "element": "string",
  "element_id": "string",
  "event_type": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dragnSurvey/latest/actions/subscribe-to-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "element": "string",
    "element_id": "string",
    "event_type": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `element` | string | yes | Element type that should trigger the webhook. |
| `element_id` | string | yes | Element id that should trigger the webhook. |
| `event_type` | string | yes | Webhook event to subscribe to. |
| `url` | string | yes | Secure endpoint that should receive the webhook call. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Drag'n Survey API returns.

## Native endpoint

Through the native Drag'n Survey API, this operation is `POST webhooks` (base URL `https://developer.dragnsurvey.com/api/v2.0.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-to-webhook.md) for the provider-specific parameters and requirements.

