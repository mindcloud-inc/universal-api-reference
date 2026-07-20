# Mentortools: Get Course Module Lesson

Retrieves a course module lesson from Mentortools.

```
GET https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/get-course-module-lesson
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mentortools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/get-course-module-lesson?connectionId=$CONNECTION_ID&lessonId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lessonId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/get-course-module-lesson?${params}`, {
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
| `lessonId` | number | yes | The lesson ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "done": true,
      "result": {
        "id": 1,
        "isActive": true,
        "lessonType": "string",
        "order": 1,
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `done` | boolean |  |
| `result.id` | number |  |
| `result.isActive` | boolean |  |
| `result.lessonType` | string |  |
| `result.order` | number |  |
| `result.title` | string |  |

## Native endpoint

Through the native Mentortools API, this operation is `GET /courses/v1/lessons/:lesson_id` (base URL `https://app.mentortools.com/public_api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-course-module-lesson.md) for the provider-specific parameters and requirements.

