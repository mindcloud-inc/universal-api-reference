# Instructure: List Todo Items

Retrieves todo items from Instructure Canvas.

```
GET https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-todo-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-todo-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-todo-items?${params}`, {
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
      "assignment": {
        "id": 1,
        "name": "Ava Chen"
      },
      "courseId": 1,
      "htmlUrl": "https://example.com",
      "ignore": true,
      "needsGradingCount": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignment.id` | number |  |
| `assignment.name` | string |  |
| `courseId` | number |  |
| `htmlUrl` | string |  |
| `ignore` | boolean |  |
| `needsGradingCount` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `GET /users/self/todo` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-todo-items.md) for the provider-specific parameters and requirements.

