# UniOne: Create Or Update Webhook

Creates or updates a webhook in UniOne.

```
POST https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/create-or-update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UniOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/create-or-update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com/unione-webhook"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/create-or-update-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com/unione-webhook"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Webhook endpoint URL. Example: `https://example.com/unione-webhook`. |
| `status` | string | no | Webhook status. Default: `active`. Example: `active`. |
| `eventFormat` | string | no | Webhook event payload format. Default: `json_post`. Example: `json_post`. |
| `deliveryInfo` | number | no | Whether to include delivery details. Default: `0`. Example: `0`. |
| `singleEvent` | number | no | Whether to send one event per callback. Default: `0`. Example: `0`. |
| `maxParallel` | number | no | Maximum parallel webhook deliveries. Default: `10`. Example: `10`. |
| `events.spamBlock` | string | no | Spam block events to subscribe to. Accepts multiple values as an array. Example: `*`. |
| `events.emailStatus` | string | no | Email status events to subscribe to. Accepts multiple values as an array. Example: `delivered`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UniOne API returns.

## Native endpoint

Through the native UniOne API, this operation is `POST webhook/set.json` (base URL `https://api.unione.io/en/transactional/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-webhook.md) for the provider-specific parameters and requirements.

