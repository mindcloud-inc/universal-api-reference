# Instructure: Create Course Section

Creates a new course section in Instructure Canvas.

```
POST https://connect.mindcloud.co/v1/universal/instructure/latest/actions/create-course-section
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/create-course-section" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "courseId": "string",
  "sectionName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instructure/latest/actions/create-course-section', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "courseId": "string",
    "sectionName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `courseId` | string | yes | Canvas course ID. |
| `sectionName` | string | yes | Name of the section. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "course_id": "string",
      "id": "string",
      "name": "Ava Chen",
      "nonxlist_course_id": "string",
      "sis_section_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `course_id` | string |  |
| `id` | string |  |
| `name` | string |  |
| `nonxlist_course_id` | string |  |
| `sis_section_id` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `POST /courses/:course_id/sections` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-course-section.md) for the provider-specific parameters and requirements.

