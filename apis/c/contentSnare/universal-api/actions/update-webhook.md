# Content Snare: Update Webhook

Updates a webhook in Content Snare.

```
PUT https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Content Snare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Webhook ID. |
| `enabled` | boolean | no | Specifies if webhook is enabled |
| `subscriptions[]` | array<string> | no | List of events associated with webhook |
| `url` | string | yes | Your webhook URL |

## Response

```json
{
  "success": true,
  "data": [
    {
      "enabled": true,
      "id": "string",
      "subscriptions": [
        [
          "string"
        ]
      ],
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enabled` | boolean |  |
| `id` | string |  |
| `subscriptions[]` | array<string> |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Content Snare API, this operation is `PUT /partner_api/v1/webhooks/{id}` (base URL `https://api.contentsnare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

