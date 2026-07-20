# Instructure: List Missing Submissions

Retrieves missing submissions from Instructure Canvas.

```
GET https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-missing-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-missing-submissions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-missing-submissions?${params}`, {
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
      "courseId": 1,
      "dueAt": "string",
      "htmlUrl": "https://example.com",
      "id": 1,
      "name": "Ava Chen",
      "pointsPossible": 1,
      "submittedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `courseId` | number |  |
| `dueAt` | string |  |
| `htmlUrl` | string |  |
| `id` | number |  |
| `name` | string |  |
| `pointsPossible` | number |  |
| `submittedAt` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `GET /users/self/missing_submissions` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-missing-submissions.md) for the provider-specific parameters and requirements.

