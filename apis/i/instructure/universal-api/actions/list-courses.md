# Instructure: List Courses

Retrieves courses from Instructure Canvas.

```
GET https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-courses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-courses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-courses?${params}`, {
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
      "courseCode": "string",
      "createdAt": "string",
      "defaultView": "string",
      "endAt": "string",
      "id": 1,
      "name": "Ava Chen",
      "startAt": "string",
      "workflowState": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `courseCode` | string |  |
| `createdAt` | string |  |
| `defaultView` | string |  |
| `endAt` | string |  |
| `id` | number |  |
| `name` | string |  |
| `startAt` | string |  |
| `workflowState` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `GET /courses` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-courses.md) for the provider-specific parameters and requirements.

