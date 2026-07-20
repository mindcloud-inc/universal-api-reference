# Innform: List Courses

Retrieves courses from Innform.

```
GET https://connect.mindcloud.co/v1/universal/innform/latest/actions/list-courses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Innform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/innform/latest/actions/list-courses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/innform/latest/actions/list-courses?${params}`, {
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
      "assignments": [
        {}
      ],
      "contentType": "string",
      "description": "string",
      "duration": 1,
      "id": "string",
      "points": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignments` | array<object> | Assignments for this course. |
| `contentType` | string | Course content type. |
| `description` | string | Course description. |
| `duration` | number | Course duration in minutes. |
| `id` | string | Course ID. |
| `points` | number | Course points. |
| `title` | string | Course title. |

## Native endpoint

Through the native Innform API, this operation is `GET /courses` (base URL `https://api.innform.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-courses.md) for the provider-specific parameters and requirements.

