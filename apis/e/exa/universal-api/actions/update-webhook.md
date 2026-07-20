# Exa: Update Webhook

Updates an existing webhook in Exa.

```
PUT https://connect.mindcloud.co/v1/universal/exa/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/exa/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/exa/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `events[]` | array<string> | no | Updated webhook events. |
| `id` | string | yes | Webhook identifier. |
| `metadata` | object | no | Updated webhook metadata object. |
| `url` | string | no | Updated HTTPS endpoint URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "events": [
        "string"
      ],
      "id": "string",
      "metadata": {},
      "object": "string",
      "secret": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `events` | array<string> | Subscribed webhook events. |
| `id` | string | Unique webhook identifier. |
| `metadata` | object | Custom metadata. |
| `object` | string | Returned object type. |
| `secret` | string | Webhook signing secret. |
| `status` | string | Webhook status. |
| `updatedAt` | date | Last update timestamp. |
| `url` | string | Webhook delivery URL. |

## Native endpoint

Through the native Exa API, this operation is `PATCH /websets/v0/webhooks/:id` (base URL `https://api.exa.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

