# Hedy: List Topic Sessions

Retrieves sessions for a Hedy topic.

```
GET https://connect.mindcloud.co/v1/universal/hedy/latest/actions/list-topic-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hedy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hedy/latest/actions/list-topic-sessions?connectionId=$CONNECTION_ID&topicId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "topicId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hedy/latest/actions/list-topic-sessions?${params}`, {
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
| `topicId` | string | yes | Unique identifier of the topic. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duration": 1,
      "id": "string",
      "startTime": "2026-05-07T12:00:00.000Z",
      "title": "string",
      "topic": {
        "color": "string",
        "description": "string",
        "iconName": "Ava Chen",
        "id": "string",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duration` | number |  |
| `id` | string |  |
| `startTime` | date |  |
| `title` | string |  |
| `topic.color` | string |  |
| `topic.description` | string |  |
| `topic.iconName` | string |  |
| `topic.id` | string |  |
| `topic.name` | string |  |

## Native endpoint

Through the native Hedy API, this operation is `GET https://api.hedy.bot/topics/:topicId/sessions` (base URL `https://api.hedy.bot`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-topic-sessions.md) for the provider-specific parameters and requirements.

