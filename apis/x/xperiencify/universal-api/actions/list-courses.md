# Xperiencify: List Courses

Retrieves courses from Xperiencify.

```
GET https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/list-courses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xperiencify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/list-courses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/list-courses?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "poster": "string",
      "slug": "string",
      "thumbnail": "string",
      "title": "string",
      "users": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `description` | string |  |
| `id` | number |  |
| `poster` | string |  |
| `slug` | string |  |
| `thumbnail` | string |  |
| `title` | string |  |
| `users` | array |  |

## Native endpoint

Through the native Xperiencify API, this operation is `GET /api/public/coach/courses/` (base URL `https://api.xperiencify.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-courses.md) for the provider-specific parameters and requirements.

