# Hightouch: Get Decision Engine Message

Retrieves a decision engine message from Hightouch.

```
GET https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/get-decision-engine-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hightouch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/get-decision-engine-message?connectionId=$CONNECTION_ID&flowId=string&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "flowId": "string",
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/get-decision-engine-message?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `flowId` | string | yes | The Decision Engine flow ID. |
| `messageId` | string | yes | The Decision Engine message ID. |

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

Through the native Hightouch API, this operation is `GET /decision-engine/flow/{flowId}/messages/{messageId}` (base URL `https://api.hightouch.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-decision-engine-message.md) for the provider-specific parameters and requirements.

