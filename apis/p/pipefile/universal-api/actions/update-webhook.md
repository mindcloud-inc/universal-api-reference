# Pipefile: Update Webhook



```
PUT https://connect.mindcloud.co/v1/universal/pipefile/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipefile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pipefile/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "event": "string",
  "target": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipefile/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "event": "string",
    "target": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Pipefile webhook ID. |
| `event` | string | yes | Updated Pipefile event that should trigger the webhook. |
| `target` | string | yes | Updated destination URL for webhook deliveries. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event": "string",
      "target": "string",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event` | string | Pipefile event that triggers the webhook. |
| `target` | string | Destination URL for webhook deliveries. |
| `user` | object | Pipefile user associated with the webhook, when returned. |

## Native endpoint

Through the native Pipefile API, this operation is `PUT /webhooks/:id/` (base URL `https://api.pipefile.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

