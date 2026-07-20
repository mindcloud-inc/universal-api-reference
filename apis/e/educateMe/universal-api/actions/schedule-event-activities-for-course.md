# EducateMe: Schedule Event Activities for Course

Schedules event activities for a course in EducateMe.

```
POST https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/schedule-event-activities-for-course
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EducateMe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/schedule-event-activities-for-course" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "courseId": "string",
  "scheduleData[]": [
    {}
  ],
  "isInZoom": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/schedule-event-activities-for-course', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "courseId": "string",
    "scheduleData[]": [{}],
    "isInZoom": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `courseId` | string | yes |  |
| `scheduleData[]` | array<object> | yes |  |
| `isInZoom` | boolean | yes |  |
| `zoomAccountEmail` | string | no |  |
| `customWebinarRoomLink` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activity": {
        "activityLink": "https://example.com",
        "id": "string",
        "title": "string"
      },
      "endingDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "linkToJoin": "https://example.com",
      "startingDate": "2026-05-07T12:00:00.000Z",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activity.activityLink` | string |  |
| `activity.id` | string |  |
| `activity.title` | string |  |
| `endingDate` | date |  |
| `id` | string |  |
| `linkToJoin` | string |  |
| `startingDate` | date |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native EducateMe API, this operation is `POST /courses/:courseId/schedule-events` (base URL `https://api.educate-me.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-event-activities-for-course.md) for the provider-specific parameters and requirements.

