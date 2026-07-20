# Planfix: Add Task Comment

Creates a new task comment in Planfix.

```
POST https://connect.mindcloud.co/v1/universal/planfix/latest/actions/add-task-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planfix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/planfix/latest/actions/add-task-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/planfix/latest/actions/add-task-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "description": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Task identifier to comment on. |
| `description` | string | yes | Comment body. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `silent` | boolean | no | Skip notifications while adding the comment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native Planfix API, this operation is `POST /task/:id/comments/` (base URL `{{credentials.accountBaseUrl}}/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-task-comment.md) for the provider-specific parameters and requirements.

