# Teach 'n Go: List Lessons

Retrieves lessons from a Teach 'n Go course.

```
GET https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/list-lessons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teach 'n Go `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/list-lessons?connectionId=$CONNECTION_ID&courseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "courseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/list-lessons?${params}`, {
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
| `courseId` | string | yes | The Teach 'n Go course ID to load lessons for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "classroom": "string",
      "courseId": 1,
      "courseTitle": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "endTime": "string",
      "id": 1,
      "isPostpone": true,
      "lessonEndDate": "string",
      "lessonStartDate": "string",
      "startTime": "string",
      "teachers": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classroom` | string |  |
| `courseId` | number |  |
| `courseTitle` | string |  |
| `date` | date |  |
| `endTime` | string |  |
| `id` | number |  |
| `isPostpone` | boolean |  |
| `lessonEndDate` | string |  |
| `lessonStartDate` | string |  |
| `startTime` | string |  |
| `teachers` | string |  |

## Native endpoint

Through the native Teach 'n Go API, this operation is `POST /globalApis/lesson_list/:course_id` (base URL `https://app.teachngo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lessons.md) for the provider-specific parameters and requirements.

