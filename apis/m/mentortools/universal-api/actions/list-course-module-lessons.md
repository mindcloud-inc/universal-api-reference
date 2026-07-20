# Mentortools: List Course Module Lessons

Retrieves lessons for a course module in Mentortools.

```
GET https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/list-course-module-lessons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mentortools `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/list-course-module-lessons?connectionId=$CONNECTION_ID&limit=25&offset=0&moduleId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "moduleId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/list-course-module-lessons?${params}`, {
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
| `moduleId` | number | yes | The module ID. |

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
          "lessonType": "string",
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
| `result[].lessonType` | string |  |
| `result[].order` | number |  |
| `result[].title` | string |  |

## Native endpoint

Through the native Mentortools API, this operation is `GET /courses/v1/modules/:module_id/lessons` (base URL `https://app.mentortools.com/public_api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-course-module-lessons.md) for the provider-specific parameters and requirements.

