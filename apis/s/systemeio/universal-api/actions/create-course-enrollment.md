# Systeme.io: Create Course Enrollment

Creates a course enrollment in Systeme.io.

```
POST https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/create-course-enrollment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Systeme.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/create-course-enrollment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "courseId": "string",
  "contactId": 1,
  "accessType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/create-course-enrollment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "courseId": "string",
    "contactId": 1,
    "accessType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `courseId` | string | yes | Course identifier. |
| `contactId` | number | yes | Contact ID to enroll in the course. |
| `accessType` | string | yes | Enrollment access type: partial_access, full_access, or dripping_content. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessType": "string",
      "active": true,
      "contact": {},
      "course": {},
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessType` | string | Enrollment access type. |
| `active` | boolean | Whether the enrollment is active. |
| `contact` | object | Enrolled contact details. |
| `course` | object | Course details for the enrollment. |
| `id` | number | Enrollment identifier. |

## Native endpoint

Through the native Systeme.io API, this operation is `POST /api/school/courses/:courseId/enrollments` (base URL `https://api.systeme.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-course-enrollment.md) for the provider-specific parameters and requirements.

