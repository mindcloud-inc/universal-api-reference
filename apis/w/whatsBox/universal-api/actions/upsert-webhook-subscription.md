# WhatsBox: Upsert Webhook Subscription

Creates or updates a webhook subscription in WhatsBox.

```
POST https://connect.mindcloud.co/v1/universal/whatsBox/latest/actions/upsert-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsBox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whatsBox/latest/actions/upsert-webhook-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "string",
  "subscriberReferenceId": "string",
  "webhookUrl": "https://example.com",
  "platform": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whatsBox/latest/actions/upsert-webhook-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "string",
    "subscriberReferenceId": "string",
    "webhookUrl": "https://example.com",
    "platform": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | string | yes | Channel ID for the WhatsApp number. |
| `subscriberReferenceId` | string | yes | Subscriber reference ID for the webhook. |
| `webhookUrl` | string | yes | Destination URL for webhook delivery. |
| `platform` | string | yes | Platform label for the webhook subscription. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "subscriberReferenceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `subscriberReferenceId` | string |  |

## Native endpoint

Through the native WhatsBox API, this operation is `POST /webhook-subscriptions` (base URL `https://api.whatsbox.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-webhook-subscription.md) for the provider-specific parameters and requirements.

