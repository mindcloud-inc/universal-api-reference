# Mentortools: List Courses

Retrieves a list of courses from Mentortools.

```
GET https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/list-courses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mentortools `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/list-courses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/list-courses?${params}`, {
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
| `archived` | boolean | no | Include archived courses. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "done": true,
      "result": [
        {
          "id": 1,
          "isActive": true,
          "order": 1,
          "title": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `done` | boolean |  |
| `result[].id` | number |  |
| `result[].isActive` | boolean |  |
| `result[].order` | number |  |
| `result[].title` | string |  |

## Native endpoint

Through the native Mentortools API, this operation is `GET /courses/v1/` (base URL `https://app.mentortools.com/public_api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-courses.md) for the provider-specific parameters and requirements.

