# Mentortools: Patch Course Module Lesson Attached Files

Updates lesson attached files in Mentortools, creating new ones when needed.

```
PUT https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/patch-course-module-lesson-attached-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mentortools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/patch-course-module-lesson-attached-files" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "lessonId": 1,
  "attachedFiles[].order": 1,
  "attachedFiles[].fileId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/patch-course-module-lesson-attached-files', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "lessonId": 1,
    "attachedFiles[].order": 1,
    "attachedFiles[].fileId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lessonId` | number | yes | The lesson ID. |
| `attachedFiles[].id` | number | no |  |
| `attachedFiles[].order` | number | yes |  |
| `attachedFiles[].fileId` | number | yes |  |

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

Through the native Mentortools API, this operation is `PATCH /courses/v1/lessons/:lesson_id/attached_files` (base URL `https://app.mentortools.com/public_api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-course-module-lesson-attached-files.md) for the provider-specific parameters and requirements.

