# Thinkific: List Course Reviews

Retrieves course review records from Thinkific.

```
GET https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/list-course-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Thinkific `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/list-course-reviews?connectionId=$CONNECTION_ID&limit=25&offset=0&courseId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "courseId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/list-course-reviews?${params}`, {
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
| `approved` | boolean | no | When true, returns only approved course reviews. |
| `courseId` | number | yes | Course ID to filter course reviews. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `meta` | object |  |

## Native endpoint

Through the native Thinkific API, this operation is `GET /course_reviews` (base URL `https://api.thinkific.com/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-course-reviews.md) for the provider-specific parameters and requirements.

