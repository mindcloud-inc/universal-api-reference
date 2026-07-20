# Hedy: Get Session To-Do Item

Retrieves a to-do item from a Hedy session.

```
GET https://connect.mindcloud.co/v1/universal/hedy/latest/actions/get-session-to-do-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hedy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hedy/latest/actions/get-session-to-do-item?connectionId=$CONNECTION_ID&sessionId=string&todoId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string",
  "todoId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hedy/latest/actions/get-session-to-do-item?${params}`, {
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
| `sessionId` | string | yes | Unique identifier of the session. |
| `todoId` | string | yes | Unique identifier of the to-do item. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed": true,
      "dueDate": "string",
      "id": "string",
      "text": "string"
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

## Native endpoint

Through the native Hedy API, this operation is `GET https://api.hedy.bot/sessions/:sessionId/todos/:todoId` (base URL `https://api.hedy.bot`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-session-to-do-item.md) for the provider-specific parameters and requirements.

