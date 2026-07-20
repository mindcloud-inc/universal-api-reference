# EducateMe: List Course Schedules

Lists course schedules in EducateMe.

```
GET https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/list-course-schedules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EducateMe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/list-course-schedules?connectionId=$CONNECTION_ID&courseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "courseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/list-course-schedules?${params}`, {
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
| `type` | string | no |  |
| `startingDate` | string | no |  |
| `endingDate` | string | no |  |

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

Through the native EducateMe API, this operation is `GET /courses/:courseId/schedules` (base URL `https://api.educate-me.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-course-schedules.md) for the provider-specific parameters and requirements.

