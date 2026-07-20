# Helpjuice: Create Webhook

Creates a new webhook in Helpjuice.

```
POST https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Helpjuice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "event": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "event": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | The webhook callback URL. |
| `event` | string | yes | The Helpjuice webhook event, for example question_create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "createdAt": "string",
      "enabledAt": "string",
      "event": "string",
      "id": 1,
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number | The Helpjuice account ID for the webhook. |
| `createdAt` | string | When the webhook was created. |
| `enabledAt` | string | When the webhook was enabled. |
| `event` | string | The Helpjuice webhook event. |
| `id` | number | The created webhook ID. |
| `updatedAt` | string | When the webhook was last updated. |
| `url` | string | The webhook callback URL. |

## Native endpoint

Through the native Helpjuice API, this operation is `POST /webhooks` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

