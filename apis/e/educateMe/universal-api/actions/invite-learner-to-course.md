# EducateMe: Invite Learner to Course

Invites a learner to a course in EducateMe.

```
POST https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/invite-learner-to-course
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EducateMe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/invite-learner-to-course" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "courseId": "cmnf0ayr5njie0874ac32t9st",
  "email": "codex.learner.one.20260331@example.com",
  "name": "Codex Learner One"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/invite-learner-to-course', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "courseId": "cmnf0ayr5njie0874ac32t9st",
    "email": "codex.learner.one.20260331@example.com",
    "name": "Codex Learner One"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `courseId` | string | yes | Course ID. Example: `cmnf0ayr5njie0874ac32t9st`. |
| `email` | string | yes | Learner email. Example: `codex.learner.one.20260331@example.com`. |
| `name` | string | yes | Learner name. Example: `Codex Learner One`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `note` | string | no | Optional learner note. Example: `Disposable test learner`. |
| `tagsIds[]` | array<string> | no | Optional tag IDs. Example: `cmnf09j0nnhpr0874u4ym8me9`. |
| `tagNames[]` | array<string> | no | Optional tag names. Example: `Codex Stage3 Tag 20260331B`. |
| `withoutConfirmation` | boolean | no | Auto-confirm learner account when true. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Learner or enrollment ID returned by EducateMe. |
| `success` | boolean | Whether the invite succeeded. |

## Native endpoint

Through the native EducateMe API, this operation is `POST /courses/:courseId/students` (base URL `https://api.educate-me.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-learner-to-course.md) for the provider-specific parameters and requirements.

