# Heyy: Create Broadcast

Creates a new broadcast in a Heyy channel.

```
POST https://connect.mindcloud.co/v1/universal/heyy/latest/actions/create-broadcast
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heyy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/heyy/latest/actions/create-broadcast" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "string",
  "name": "Ava Chen",
  "workflowId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heyy/latest/actions/create-broadcast', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "string",
    "name": "Ava Chen",
    "workflowId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | string | yes | The Heyy channel ID. |
| `contacts[]` | array<object> | no | The contacts payload. |
| `isReoccurring` | boolean | no | Whether the broadcast repeats. |
| `isScheduled` | boolean | no | Whether the broadcast is scheduled. |
| `messageTemplateId` | string | no | The message template ID. |
| `name` | string | yes | The broadcast name. |
| `recurrenceRules[]` | array<string> | no | The recurrence rules array. |
| `scheduledAt` | string | no | When the broadcast should run. |
| `variables[]` | array<object> | no | The broadcast variables. |
| `workflowId` | string | yes | The workflow ID used by the broadcast. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workflowId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelId` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `workflowId` | string |  |

## Native endpoint

Through the native Heyy API, this operation is `POST /[:channelId]/broadcasts` (base URL `https://api.heyy.io/api/v2.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-broadcast.md) for the provider-specific parameters and requirements.

