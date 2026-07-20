# Hedy: List Topics

Retrieves topics from Hedy.

```
GET https://connect.mindcloud.co/v1/universal/hedy/latest/actions/list-topics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hedy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hedy/latest/actions/list-topics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hedy/latest/actions/list-topics?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Hedy API, this operation is `GET https://api.hedy.bot/topics` (base URL `https://api.hedy.bot`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-topics.md) for the provider-specific parameters and requirements.

