# LaGrowthMachine: Create Inbox Webhook

Creates an inbox webhook in LaGrowthMachine.

```
POST https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/create-inbox-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaGrowthMachine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/create-inbox-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/create-inbox-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaigns[]` | array<string> | no | Campaign IDs to scope the webhook to, or `all`. |
| `description` | string | no | Optional description for the webhook. |
| `name` | string | yes | Display name of the webhook. |
| `url` | string | yes | Public URL that receives webhook events. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audiences": [
        [
          "string"
        ]
      ],
      "campaigns": [
        [
          "string"
        ]
      ],
      "createdAt": "string",
      "id": "string",
      "key": "string",
      "tags": [
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
| `audiences[]` | array<string> | Audience identifiers scoped to the webhook. |
| `campaigns[]` | array<string> | Campaign identifiers scoped to the webhook. |
| `createdAt` | string | Webhook creation timestamp. |
| `id` | string | Webhook identifier. |
| `key` | string | Webhook display label returned by LaGrowthMachine. |
| `tags[]` | array<string> | Tag filters applied to the webhook. |
| `type` | string | Webhook event type. |
| `url` | string | Webhook target URL. |

## Native endpoint

Through the native LaGrowthMachine API, this operation is `POST /inboxWebhooks` (base URL `https://apiv2.lagrowthmachine.com/flow`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-inbox-webhook.md) for the provider-specific parameters and requirements.

