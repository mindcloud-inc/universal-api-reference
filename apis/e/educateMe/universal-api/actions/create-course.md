# EducateMe: Create Course

Creates a new course in EducateMe.

```
POST https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/create-course
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EducateMe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/create-course" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "Codex Disposable Course 20260331",
  "previewUrl": "https://example.com/course-preview",
  "withProgramSyncing": "false",
  "type": "SELF_PACED"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/create-course', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "Codex Disposable Course 20260331",
    "previewUrl": "https://example.com/course-preview",
    "withProgramSyncing": "false",
    "type": "SELF_PACED"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Course title. Example: `Codex Disposable Course 20260331`. |
| `previewUrl` | string | yes | Course preview URL. Example: `https://example.com/course-preview`. |
| `withProgramSyncing` | boolean | yes | Whether program syncing is enabled. Default: `false`. |
| `type` | string | yes | Course type. Allowed values: COHORT_BASED, SELF_PACED. One of: `0`, `1`. Example: `SELF_PACED`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `duplicatedCourseId` | string | no | Optional course ID to copy structure from. Example: `cmnf123courseid`. |
| `instructorEmails[]` | array<string> | no | Optional instructor emails. Example: `apps@mindcloud.co`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletedAt": {},
      "id": "string",
      "instructors": [
        {
          "email": "ava@example.com",
          "id": "string"
        }
      ],
      "isFinished": true,
      "isSuspended": true,
      "previewUrl": "https://example.com",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletedAt` | object |  |
| `id` | string |  |
| `instructors[].email` | string |  |
| `instructors[].id` | string |  |
| `isFinished` | boolean |  |
| `isSuspended` | boolean |  |
| `previewUrl` | string |  |
| `title` | string |  |

## Native endpoint

Through the native EducateMe API, this operation is `POST /courses` (base URL `https://api.educate-me.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-course.md) for the provider-specific parameters and requirements.

