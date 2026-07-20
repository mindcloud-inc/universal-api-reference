# EducateMe: Remove Learner from Course

Removes a learner from a course in EducateMe.

```
DELETE https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/remove-learner-from-course
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EducateMe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/remove-learner-from-course?connectionId=$CONNECTION_ID&courseId=cmnf0ayr5njie0874ac32t9st&email=codex.learner.one.20260331%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "courseId": "cmnf0ayr5njie0874ac32t9st",
  "email": "codex.learner.one.20260331@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/remove-learner-from-course?${params}`, {
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
| `courseId` | string | yes | Course ID. Example: `cmnf0ayr5njie0874ac32t9st`. |
| `email` | string | yes | Learner email. Example: `codex.learner.one.20260331@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the learner was removed from the course successfully. |

## Native endpoint

Through the native EducateMe API, this operation is `POST /courses/:courseId/students/unassign` (base URL `https://api.educate-me.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-learner-from-course.md) for the provider-specific parameters and requirements.

