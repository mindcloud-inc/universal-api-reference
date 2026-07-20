# Xperiencify: Add Student to Course

Creates a student enrollment in an Xperiencify course.

```
POST https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/add-student-to-course
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xperiencify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/add-student-to-course" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "studentEmail": "ava@example.com",
  "firstName": "Ava",
  "courseId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/add-student-to-course', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "studentEmail": "ava@example.com",
    "firstName": "Ava",
    "courseId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `studentEmail` | string | yes | Email address for the student. |
| `firstName` | string | yes | Student first name. |
| `lastName` | string | no | Student last name. |
| `phone` | string | no | Student phone number. |
| `courseId` | number | yes | Course to enroll the student in. |
| `password` | string | no | Optional password for the student. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "magicLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `magicLink` | string | Magic login link returned after successful student creation. |

## Native endpoint

Through the native Xperiencify API, this operation is `POST /api/public/student/create/` (base URL `https://api.xperiencify.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-student-to-course.md) for the provider-specific parameters and requirements.

