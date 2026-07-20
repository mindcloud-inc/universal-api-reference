# Documently: Create Webhook

Creates a new webhook in Documently.

```
POST https://connect.mindcloud.co/v1/universal/documently/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documently/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documently/latest/actions/create-webhook', {
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
| `active` | boolean | no | Whether the webhook is active. |
| `events[]` | array<string> | no | Webhook event names. |
| `project` | string | no | Project ID for the webhook. |
| `url` | string | no | Public callback URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@context": "string",
      "@id": "string",
      "@type": "string",
      "active": true,
      "events": [
        "string"
      ],
      "id": "string",
      "project": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@context` | string |  |
| `@id` | string |  |
| `@type` | string |  |
| `active` | boolean |  |
| `events` | array<string> |  |
| `id` | string |  |
| `project` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Documently API, this operation is `POST /webhooks` (base URL `https://app.documently.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

