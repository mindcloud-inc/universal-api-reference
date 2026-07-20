# Instructure: Get Enrollment

Retrieves an enrollment from Instructure Canvas.

```
GET https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-enrollment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-enrollment?connectionId=$CONNECTION_ID&courseId=1&enrollmentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "courseId": "1",
  "enrollmentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-enrollment?${params}`, {
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
| `courseId` | string | yes | The Canvas course ID. Default: `1`. |
| `enrollmentId` | string | yes | The Canvas enrollment ID. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "courseId": 1,
      "createdAt": "string",
      "enrollmentState": "string",
      "id": 1,
      "lastActivityAt": "string",
      "role": "string",
      "type": "string",
      "updatedAt": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `courseId` | number |  |
| `createdAt` | string |  |
| `enrollmentState` | string |  |
| `id` | number |  |
| `lastActivityAt` | string |  |
| `role` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Instructure API, this operation is `GET /courses/:course_id/enrollments/:enrollment_id` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-enrollment.md) for the provider-specific parameters and requirements.

