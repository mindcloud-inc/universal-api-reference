# Hightouch: Update Decision Engine Message

Updates a decision engine message in Hightouch.

```
PUT https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/update-decision-engine-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hightouch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/update-decision-engine-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "flowId": "string",
  "messageId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/update-decision-engine-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "flowId": "string",
    "messageId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `flowId` | string | yes | The Decision Engine flow ID. |
| `name` | string | no | The message name. |
| `messageId` | string | yes | The Decision Engine message ID. |
| `config` | object | no | Message configuration object. |
| `tags` | object | no | Message tags. |
| `guardrails` | object | no | Message guardrail settings. |
| `variables[]` | array<object> | no | Message variables. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelId": "string",
      "config": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "guardrails": {},
      "id": "string",
      "name": "Ava Chen",
      "tags": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "variables": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelId` | string | Message channel ID. |
| `config` | object | Message configuration. |
| `createdAt` | date | Creation timestamp. |
| `guardrails` | object | Message guardrails. |
| `id` | string | Decision engine message ID. |
| `name` | string | Decision engine message name. |
| `tags` | object | Message tags. |
| `updatedAt` | date | Last update timestamp. |
| `variables` | array<object> | Message variables. |

## Native endpoint

Through the native Hightouch API, this operation is `PATCH /decision-engine/flow/{flowId}/messages/{messageId}` (base URL `https://api.hightouch.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-decision-engine-message.md) for the provider-specific parameters and requirements.

