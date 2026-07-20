# Mentortools: Patch Course

Updates part of an existing course in Mentortools.

```
PUT https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/patch-course
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mentortools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/patch-course" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "courseId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/patch-course', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "courseId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `courseId` | number | yes | The course ID. |
| `title` | string | no | Title of the course, if not provided, it will not be updated. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "done": true,
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `done` | boolean |  |
| `result` | boolean |  |

## Native endpoint

Through the native Mentortools API, this operation is `PATCH /courses/v1/:course_id` (base URL `https://app.mentortools.com/public_api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-course.md) for the provider-specific parameters and requirements.

