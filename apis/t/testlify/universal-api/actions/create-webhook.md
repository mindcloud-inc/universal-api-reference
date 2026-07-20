# Testlify: Create Webhook

Creates a webhook subscription in Testlify.

```
POST https://connect.mindcloud.co/v1/universal/testlify/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/testlify/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "payloadUrl": "https://example.com",
  "events[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testlify/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "payloadUrl": "https://example.com",
    "events[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Webhook name. |
| `payloadUrl` | string | yes | Webhook destination URL. |
| `events[]` | array<string> | yes | Webhook event names. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "endpointId": "string",
      "events": [
        "string"
      ],
      "id": "string",
      "modified": "string",
      "name": "Ava Chen",
      "orgId": "string",
      "payloadUrl": "https://example.com",
      "restructureBySchema": true,
      "subscriptionId": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `endpointId` | string |  |
| `events` | array<string> |  |
| `id` | string |  |
| `modified` | string |  |
| `name` | string |  |
| `orgId` | string |  |
| `payloadUrl` | string |  |
| `restructureBySchema` | boolean |  |
| `subscriptionId` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Testlify API, this operation is `POST /v1/webhook` (base URL `https://api.testlify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

