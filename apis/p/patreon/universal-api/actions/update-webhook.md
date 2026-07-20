# Patreon: Update Webhook

Updates an existing webhook in Patreon.

```
PUT https://connect.mindcloud.co/v1/universal/patreon/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Patreon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/patreon/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/patreon/latest/actions/update-webhook', {
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
| `paused` | boolean | no | Patreon accepts false to resume a failed webhook and retry queued events when available. Setting true is rejected by the API. |
| `triggers[]` | array<string> | no | The Patreon webhook events to subscribe to. |
| `uri` | string | no | The fully qualified URL that Patreon should call. |
| `webhookId` | string | yes | The Patreon webhook ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "links": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `links` | object |  |

## Native endpoint

Through the native Patreon API, this operation is `PATCH /webhooks/:webhookId` (base URL `https://www.patreon.com/api/oauth2/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

