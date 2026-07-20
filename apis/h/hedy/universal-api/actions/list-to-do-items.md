# Hedy: List To-Do Items

Retrieves to-do items from Hedy.

```
GET https://connect.mindcloud.co/v1/universal/hedy/latest/actions/list-to-do-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hedy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hedy/latest/actions/list-to-do-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hedy/latest/actions/list-to-do-items?${params}`, {
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
      "completed": true,
      "dueDate": "string",
      "id": "string",
      "sessionId": "string",
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
| `sessionId` | string |  |
| `text` | string |  |
| `topic.color` | string |  |
| `topic.description` | string |  |
| `topic.iconName` | string |  |
| `topic.id` | string |  |
| `topic.name` | string |  |

## Native endpoint

Through the native Hedy API, this operation is `GET https://api.hedy.bot/todos` (base URL `https://api.hedy.bot`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-to-do-items.md) for the provider-specific parameters and requirements.

