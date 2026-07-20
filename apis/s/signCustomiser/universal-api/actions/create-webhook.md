# Sign Customiser: Create Webhook

Creates a new webhook subscription in Sign Customiser.

```
POST https://connect.mindcloud.co/v1/universal/signCustomiser/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sign Customiser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signCustomiser/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "topic": "form:submitted",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signCustomiser/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "topic": "form:submitted",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `topic` | list | yes | The event topic to subscribe to. One of: `form:submitted`, `order:created`, `product:created`. |
| `url` | string | yes | The URL where webhook payloads will be sent. |
| `meta` | object | no | Optional metadata to store with the webhook. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "meta": {},
      "ownerId": 1,
      "ownerType": "string",
      "secret": "string",
      "status": "string",
      "topic": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "webhookId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `meta` | object |  |
| `ownerId` | number |  |
| `ownerType` | string |  |
| `secret` | string |  |
| `status` | string |  |
| `topic` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `webhookId` | number |  |

## Native endpoint

Through the native Sign Customiser API, this operation is `POST /api/v2/webhooks` (base URL `https://web.signcustomiser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

