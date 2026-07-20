# EducateMe: List Learners' Assignments by Course

Lists learner assignments for a course in EducateMe.

```
GET https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/list-learners-assignments-by-course
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EducateMe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/list-learners-assignments-by-course?connectionId=$CONNECTION_ID&courseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "courseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/list-learners-assignments-by-course?${params}`, {
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
| `courseId` | string | yes |  |
| `status` | string | no |  |
| `student_email` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EducateMe API returns.

## Native endpoint

Through the native EducateMe API, this operation is `GET /courses/:courseId/students-assignments` (base URL `https://api.educate-me.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-learners-assignments-by-course.md) for the provider-specific parameters and requirements.

