# Sign Customiser: Update Webhook

Updates an existing webhook subscription in Sign Customiser.

```
PUT https://connect.mindcloud.co/v1/universal/signCustomiser/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sign Customiser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/signCustomiser/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookId": 1,
  "topic": "form:submitted",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signCustomiser/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhookId": 1,
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
| `webhookId` | number | yes | The ID of the webhook. |
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
      "externalId": "string",
      "meta": {},
      "owner": {},
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
| `externalId` | string |  |
| `meta` | object |  |
| `owner` | object |  |
| `ownerId` | number |  |
| `ownerType` | string |  |
| `secret` | string |  |
| `status` | string |  |
| `topic` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `webhookId` | number |  |

## Native endpoint

Through the native Sign Customiser API, this operation is `PUT /api/v2/webhooks/:webhookId` (base URL `https://web.signcustomiser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

