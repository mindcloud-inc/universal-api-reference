# Sarbacane: Add Webhook

Creates a new webhook in Sarbacane.

```
POST https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/add-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sarbacane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/add-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/add-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `displayName` | string | no | Webhook display name. |
| `kinds` | string | no | Webhook event kinds array. |
| `url` | string | no | Webhook destination URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "id": "string",
      "kinds": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string | Webhook display name. |
| `id` | string | Sarbacane webhook ID. |
| `kinds` | array<string> | Subscribed webhook event kinds. |
| `url` | string | Webhook destination URL. |

## Native endpoint

Through the native Sarbacane API, this operation is `POST /webhooks` (base URL `https://api.sarbacane.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-webhook.md) for the provider-specific parameters and requirements.

