# Mentortools: List Course Module Lesson Content Blocks

Retrieves lesson content blocks from Mentortools.

```
GET https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/list-course-module-lesson-content-blocks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mentortools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/list-course-module-lesson-content-blocks?connectionId=$CONNECTION_ID&lessonId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lessonId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/list-course-module-lesson-content-blocks?${params}`, {
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
| `lessonId` | number | yes | The lesson ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "done": true,
      "result": [
        {
          "blockType": "string",
          "id": 1,
          "isExpanded": true,
          "order": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `done` | boolean |  |
| `result[].blockType` | string |  |
| `result[].id` | number |  |
| `result[].isExpanded` | boolean |  |
| `result[].order` | number |  |

## Native endpoint

Through the native Mentortools API, this operation is `GET /courses/v1/lessons/:lesson_id/content_blocks` (base URL `https://app.mentortools.com/public_api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-course-module-lesson-content-blocks.md) for the provider-specific parameters and requirements.

