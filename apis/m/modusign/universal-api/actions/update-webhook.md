# Modusign: Update Webhook

Updates an existing webhook in Modusign.

```
PUT https://connect.mindcloud.co/v1/universal/modusign/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/modusign/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/modusign/latest/actions/update-webhook', {
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
| `webhookId` | string | yes | The Modusign webhook ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "events": [
        "string"
      ],
      "headers": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
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
| `createdAt` | string | The creation timestamp. |
| `events` | array<string> | Subscribed webhook events. |
| `headers` | array<object> | Additional webhook headers. |
| `id` | string | The webhook ID. |
| `name` | string | The webhook name. |
| `updatedAt` | string | The update timestamp. |
| `url` | string | The webhook callback URL. |

## Native endpoint

Through the native Modusign API, this operation is `PUT /webhooks/:webhookId` (base URL `https://api.modusign.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

