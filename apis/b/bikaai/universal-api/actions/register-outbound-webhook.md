# Bika.ai: Register Outbound Webhook

Creates an outbound webhook in Bika.ai.

```
POST https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/register-outbound-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bika.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/register-outbound-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": "string",
  "eventType": "string",
  "name": "Ava Chen",
  "callbackURL": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/register-outbound-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": "string",
    "eventType": "string",
    "name": "Ava Chen",
    "callbackURL": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `spaceId` | string | yes | Bika.ai workspace/space ID. |
| `eventType` | string | yes | Webhook event type such as ON_RECORD_CREATED. |
| `name` | string | yes | Webhook name. |
| `callbackURL` | string | yes | HTTPS URL that Bika.ai should call when the webhook event occurs. |
| `description` | string | no | Webhook description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "callbackURL": "https://example.com",
        "description": "string",
        "eventType": "string",
        "id": "string",
        "name": "Ava Chen",
        "node": {
          "id": "string",
          "name": "Ava Chen",
          "type": "string"
        }
      },
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | object |  |
| `data.callbackURL` | string |  |
| `data.description` | string |  |
| `data.eventType` | string |  |
| `data.id` | string |  |
| `data.name` | string |  |
| `data.node` | object |  |
| `data.node.id` | string |  |
| `data.node.name` | string |  |
| `data.node.type` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Bika.ai API, this operation is `POST /spaces/:spaceId/outgoing-webhooks` (base URL `https://bika.ai/api/openapi/bika/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-outbound-webhook.md) for the provider-specific parameters and requirements.

