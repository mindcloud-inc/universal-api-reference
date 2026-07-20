# Pixela: Create Webhook

Creates a new webhook in Pixela.

```
POST https://connect.mindcloud.co/v1/universal/pixela/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pixela `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pixela/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "username": "Ava Chen",
  "graph_id": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pixela/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "username": "Ava Chen",
    "graph_id": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `username` | string | yes | Pixela username in the request path. |
| `graph_id` | string | yes | Target graph ID for the webhook. |
| `type` | string | yes | Webhook behavior: increment, decrement, add, subtract, or stopwatch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isSuccess": true,
      "message": "string",
      "webhookHash": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isSuccess` | boolean |  |
| `message` | string |  |
| `webhookHash` | string |  |

## Native endpoint

Through the native Pixela API, this operation is `POST /v1/users/:username/webhooks` (base URL `https://pixe.la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

