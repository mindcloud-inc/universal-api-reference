# Easy Projects: Get Task Types

Retrieves task types from Easy Projects.

```
GET https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-task-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy Projects `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-task-types?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-task-types?${params}`, {
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
      "defaultCompletedStatusId": 1,
      "defaultStatusId": 1,
      "id": 1,
      "name": "Ava Chen",
      "statuses": [
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
| `defaultCompletedStatusId` | number |  |
| `defaultStatusId` | number |  |
| `id` | number |  |
| `name` | string |  |
| `statuses` | array<object> |  |

## Native endpoint

Through the native Easy Projects API, this operation is `GET /api/v1/task-types` (base URL `https://api.go.easyprojects.net/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-task-types.md) for the provider-specific parameters and requirements.

