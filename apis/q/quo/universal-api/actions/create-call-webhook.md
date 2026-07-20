# Quo: Create Call Webhook

Creates a new webhook for Quo calls.

```
POST https://connect.mindcloud.co/v1/universal/quo/latest/actions/create-call-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quo/latest/actions/create-call-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "events[]": [
    "string"
  ],
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quo/latest/actions/create-call-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "events[]": ["string"],
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `events[]` | array<string> | yes |  |
| `url` | string | yes |  |
| `label` | string | no |  |
| `resourceIds[]` | array<string> | no |  |
| `status` | string | no |  |
| `userId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "events": [
        "string"
      ],
      "id": "string",
      "key": "string",
      "label": "string",
      "orgId": "string",
      "resourceIds": [
        "string"
      ],
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
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
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `events` | array<string> |  |
| `id` | string |  |
| `key` | string |  |
| `label` | string |  |
| `orgId` | string |  |
| `resourceIds` | array<string> |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Quo API, this operation is `POST /webhooks/calls` (base URL `https://api.openphone.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-call-webhook.md) for the provider-specific parameters and requirements.

