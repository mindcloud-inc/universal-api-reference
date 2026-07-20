# Hireflix: Update Webhook

Updates an existing webhook in Hireflix.

```
PUT https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hireflix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.id` | string | yes | The Hireflix webhook ID. |
| `variables.url` | string | no | The destination URL for webhook deliveries. |
| `variables.events` | string | no | The webhook event types to subscribe to. Accepts multiple values as an array. |
| `variables.active` | boolean | no | Whether the webhook should remain active. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "events": [
        "string"
      ],
      "external": "string",
      "id": "string",
      "owner": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `events` | array<string> |  |
| `external` | string |  |
| `id` | string |  |
| `owner` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Hireflix API, this operation is `POST me` (base URL `https://api.hireflix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

