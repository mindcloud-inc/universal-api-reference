# Seam: Create Webhook

Creates a new webhook in Seam.

```
POST https://connect.mindcloud.co/v1/universal/seam/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seam/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seam/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventTypes` | list<string> | no |  |
| `url` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "secret": "string",
      "url": "https://example.com",
      "webhookId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `secret` | string |  |
| `url` | string |  |
| `webhookId` | string |  |

## Native endpoint

Through the native Seam API, this operation is `POST /webhooks/create` (base URL `https://connect.getseam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

