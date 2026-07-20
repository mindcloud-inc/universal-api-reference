# Pipedream: Create a webhook

Creates a new webhook in Pipedream.

```
POST https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/create-a-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/create-a-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "description": "string",
  "name": "Ava Chen",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/create-a-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "description": "string",
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
| `description` | string | yes | The description to assign to the webhook. |
| `name` | string | yes | The name to assign to the webhook. |
| `url` | string | yes | The HTTP or HTTPS endpoint URL where events should be delivered. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "createdAt": 1,
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": 1,
      "url": "https://example.com",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `createdAt` | number |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `updatedAt` | number |  |
| `url` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Pipedream API, this operation is `POST /webhooks` (base URL `https://api.pipedream.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-webhook.md) for the provider-specific parameters and requirements.

