# Mentortools: Update Course

Updates an existing course in Mentortools.

```
PUT https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/update-course
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mentortools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/update-course" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "courseId": 1,
  "title": "string",
  "order": 1,
  "isActive": true,
  "isSecret": true,
  "isArchived": true,
  "isDisplayedInApp": true,
  "isOfflineDownloadable": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/update-course', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "courseId": 1,
    "title": "string",
    "order": 1,
    "isActive": true,
    "isSecret": true,
    "isArchived": true,
    "isDisplayedInApp": true,
    "isOfflineDownloadable": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `courseId` | number | yes | The course ID. |
| `title` | string | yes | Title of the course. |
| `order` | number | yes | Order of the course in the list. |
| `isActive` | boolean | yes | Whether the course is active and available for users. |
| `isSecret` | boolean | yes | Whether the course is secret. |
| `isArchived` | boolean | yes | Whether the course is archived. |
| `isDisplayedInApp` | boolean | yes | Whether the course is displayed in mobile app. |
| `isOfflineDownloadable` | boolean | yes | Whether the course can be downloaded for offline access. |

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

Through the native Mentortools API, this operation is `PUT /courses/v1/:course_id` (base URL `https://app.mentortools.com/public_api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-course.md) for the provider-specific parameters and requirements.

