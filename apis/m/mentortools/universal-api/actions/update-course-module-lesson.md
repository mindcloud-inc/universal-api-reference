# Mentortools: Update Course Module Lesson

Updates an existing course module lesson in Mentortools.

```
PUT https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/update-course-module-lesson
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mentortools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/update-course-module-lesson" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "lessonId": 1,
  "lessonType": "string",
  "title": "string",
  "isActive": true,
  "isPublished": true,
  "mandatory": true,
  "order": 1,
  "contentBlocks[].blockType": "string",
  "contentBlocks[].order": 1,
  "attachedFiles[].order": 1,
  "attachedFiles[].fileId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/update-course-module-lesson', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "lessonId": 1,
    "lessonType": "string",
    "title": "string",
    "isActive": true,
    "isPublished": true,
    "mandatory": true,
    "order": 1,
    "contentBlocks[].blockType": "string",
    "contentBlocks[].order": 1,
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
| `lessonType` | string | yes | Type of the lesson. |
| `title` | string | yes | Title of the lesson. |
| `isActive` | boolean | yes | Whether the lesson is active. |
| `isPublished` | boolean | yes | Whether the lesson is published. |
| `mandatory` | boolean | yes | Whether the lesson is mandatory. |
| `order` | number | yes | Order of the lesson. |
| `contentBlocks[].id` | number | no |  |
| `contentBlocks[].blockType` | string | yes |  |
| `contentBlocks[].order` | number | yes |  |
| `contentBlocks[].isExpanded` | boolean | no |  |
| `contentBlocks[].content.payload` | string | no |  |
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

Through the native Mentortools API, this operation is `PUT /courses/v1/lessons/:lesson_id` (base URL `https://app.mentortools.com/public_api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-course-module-lesson.md) for the provider-specific parameters and requirements.

