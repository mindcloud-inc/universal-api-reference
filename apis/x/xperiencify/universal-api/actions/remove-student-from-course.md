# Xperiencify: Remove Student From Course

Deletes a student's enrollment from an Xperiencify course.

```
DELETE https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/remove-student-from-course
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xperiencify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/remove-student-from-course?connectionId=$CONNECTION_ID&studentEmail=ava%40example.com&courseId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "studentEmail": "ava@example.com",
  "courseId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/remove-student-from-course?${params}`, {
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
| `studentEmail` | string | yes | Email address for the student. |
| `courseId` | number | yes | Course to remove the student from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Result message from the course removal request. |

## Native endpoint

Through the native Xperiencify API, this operation is `POST /api/public/student/course/remove/` (base URL `https://api.xperiencify.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-student-from-course.md) for the provider-specific parameters and requirements.

