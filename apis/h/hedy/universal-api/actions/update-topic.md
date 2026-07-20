# Hedy: Update Topic

Updates an existing topic in Hedy.

```
PUT https://connect.mindcloud.co/v1/universal/hedy/latest/actions/update-topic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hedy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hedy/latest/actions/update-topic" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "topicId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hedy/latest/actions/update-topic', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "topicId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `color` | string | no | New hex color code. |
| `description` | string | no | New description for the topic. |
| `iconName` | string | no | New material icon name. |
| `name` | string | no | New name for the topic. |
| `topicContext` | string | no | New custom instructions for this topic. |
| `topicId` | string | yes | Unique identifier of the topic. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "dominantSessionType": "string",
      "iconName": "Ava Chen",
      "id": "string",
      "lastSessionDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "sessionCount": 1,
      "topicContext": "string",
      "topicContextUpdatedAt": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `dominantSessionType` | string |  |
| `iconName` | string |  |
| `id` | string |  |
| `lastSessionDate` | date |  |
| `name` | string |  |
| `sessionCount` | number |  |
| `topicContext` | string |  |
| `topicContextUpdatedAt` | date |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Hedy API, this operation is `PATCH https://api.hedy.bot/topics/:topicId` (base URL `https://api.hedy.bot`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-topic.md) for the provider-specific parameters and requirements.

