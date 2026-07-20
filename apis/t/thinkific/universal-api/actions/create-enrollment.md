# Thinkific: Create Enrollment

Creates a new enrollment in Thinkific.

```
POST https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/create-enrollment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Thinkific `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/create-enrollment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "courseId": 1,
  "userId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/create-enrollment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "courseId": 1,
    "userId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activatedAt` | date | no | Enrollment activation timestamp. |
| `courseId` | number | yes | Course to enroll the user in. |
| `expiryDate` | date | no | Enrollment expiry date. |
| `userId` | number | yes | User to enroll. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activatedAt": "string",
      "completed": true,
      "completedAt": "string",
      "courseId": 1,
      "courseName": "Ava Chen",
      "expired": true,
      "expiryDate": "string",
      "id": 1,
      "isFreeTrial": true,
      "percentageCompleted": 1,
      "startedAt": "string",
      "updatedAt": "string",
      "userEmail": "ava@example.com",
      "userId": 1,
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activatedAt` | string |  |
| `completed` | boolean |  |
| `completedAt` | string |  |
| `courseId` | number |  |
| `courseName` | string |  |
| `expired` | boolean |  |
| `expiryDate` | string |  |
| `id` | number |  |
| `isFreeTrial` | boolean |  |
| `percentageCompleted` | number |  |
| `startedAt` | string |  |
| `updatedAt` | string |  |
| `userEmail` | string |  |
| `userId` | number |  |
| `userName` | string |  |

## Native endpoint

Through the native Thinkific API, this operation is `POST /enrollments` (base URL `https://api.thinkific.com/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-enrollment.md) for the provider-specific parameters and requirements.

