# WaiverForever: Subscribe an Event

Creates a webhook subscription in WaiverForever.

```
POST https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/subscribe-an-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverForever `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/subscribe-an-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event": "string",
  "targetUrl": "https://example.com",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/subscribe-an-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event": "string",
    "targetUrl": "https://example.com",
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `event` | string | yes | Webhook event name to subscribe to. |
| `targetUrl` | string | yes | Callback URL that receives webhook events. |
| `templateId` | string | yes | Template to subscribe against. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": "string",
      "disabled": true,
      "event": "string",
      "id": "string",
      "secretKey": "string",
      "state": "string",
      "targetUrl": "https://example.com",
      "templateId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | string | Actor that created the subscription. |
| `disabled` | boolean | Whether the subscription is disabled. |
| `event` | string | Subscribed event name. |
| `id` | string | Webhook subscription identifier. |
| `secretKey` | string | Secret key used to sign webhook payloads. |
| `state` | string | Provider state string for the subscription. |
| `targetUrl` | string | Webhook callback URL. |
| `templateId` | string | Template attached to the subscription. |

## Native endpoint

Through the native WaiverForever API, this operation is `POST /openapi/v1/webhooks/` (base URL `https://api.waiverforever.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-an-event.md) for the provider-specific parameters and requirements.

