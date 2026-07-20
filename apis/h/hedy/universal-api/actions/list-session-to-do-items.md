# Hedy: List Session To-Do Items

Retrieves to-do items for a Hedy session.

```
GET https://connect.mindcloud.co/v1/universal/hedy/latest/actions/list-session-to-do-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hedy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hedy/latest/actions/list-session-to-do-items?connectionId=$CONNECTION_ID&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hedy/latest/actions/list-session-to-do-items?${params}`, {
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
| `format` | string | no | Set to zapier to receive a flat array response suitable for Zapier triggers. |
| `sessionId` | string | yes | Unique identifier of the session. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed": true,
      "dueDate": "string",
      "id": "string",
      "text": "string",
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
| `completed` | boolean |  |
| `dueDate` | string |  |
| `id` | string |  |
| `text` | string |  |
| `topic.color` | string |  |
| `topic.description` | string |  |
| `topic.iconName` | string |  |
| `topic.id` | string |  |
| `topic.name` | string |  |

## Native endpoint

Through the native Hedy API, this operation is `GET https://api.hedy.bot/sessions/:sessionId/todos` (base URL `https://api.hedy.bot`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-session-to-do-items.md) for the provider-specific parameters and requirements.

