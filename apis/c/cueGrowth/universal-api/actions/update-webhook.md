# CueGrowth: Update Webhook



```
PUT https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CueGrowth `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhookId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookId` | string | yes | ID of the webhook. |
| `name` | string | no | Name of the webhook. |
| `active` | boolean | no | Controls whether the webhook is active. |
| `url` | string | no | URL of the webhook. |
| `eventTypes[]` | array<string> | no | Events that trigger the webhook. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "event_types": [
        [
          "string"
        ]
      ],
      "id": 1,
      "name": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `event_types[]` | array<string> |  |
| `id` | number |  |
| `name` | string |  |
| `url` | string |  |

## Native endpoint

Through the native CueGrowth API, this operation is `PUT /webhooks/{webhook_id}/update` (base URL `https://api.cuegrowth.ai/public/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

