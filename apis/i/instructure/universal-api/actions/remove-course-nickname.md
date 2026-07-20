# Instructure: Remove Course Nickname

Deletes a course nickname from Instructure Canvas.

```
DELETE https://connect.mindcloud.co/v1/universal/instructure/latest/actions/remove-course-nickname
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/remove-course-nickname?connectionId=$CONNECTION_ID&courseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "courseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/remove-course-nickname?${params}`, {
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
| `courseId` | string | yes | Canvas course ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "course_id": "string",
      "name": "Ava Chen",
      "nickname": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `course_id` | string |  |
| `name` | string |  |
| `nickname` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `DELETE /users/self/course_nicknames/:course_id` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-course-nickname.md) for the provider-specific parameters and requirements.

