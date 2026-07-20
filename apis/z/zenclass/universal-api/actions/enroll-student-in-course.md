# Zenclass: Enroll student in course

Enrolls an existing student in a Zenclass course.

```
POST https://connect.mindcloud.co/v1/universal/zenclass/latest/actions/enroll-student-in-course
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenclass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zenclass/latest/actions/enroll-student-in-course" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "courseId": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zenclass/latest/actions/enroll-student-in-course', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "courseId": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `courseId` | string | yes | Zenclass course UUID. |
| `email` | string | yes | Student email address. |
| `sendEmail` | boolean | no | Whether Zenclass should email the student. |
| `tariffId` | string | no | Course tariff UUID. |
| `validTo` | date | no | Access expiration timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "course_id": "string",
      "tariff_id": "string",
      "user_id": "string",
      "valid_to": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `course_id` | string | Course UUID. |
| `tariff_id` | string | Tariff UUID when one is applied. |
| `user_id` | string | Student UUID. |
| `valid_to` | date | Course access expiration timestamp. |

## Native endpoint

Through the native Zenclass API, this operation is `POST /api/v1/student/course/enroll` (base URL `https://api.zenclass.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enroll-student-in-course.md) for the provider-specific parameters and requirements.

