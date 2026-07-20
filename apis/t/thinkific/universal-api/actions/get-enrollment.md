# Thinkific: Get Enrollment

Retrieves an enrollment record from Thinkific.

```
GET https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/get-enrollment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Thinkific `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/get-enrollment?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/get-enrollment?${params}`, {
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
| `id` | number | yes | Enrollment identifier. |

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

Through the native Thinkific API, this operation is `GET /enrollments/:id` (base URL `https://api.thinkific.com/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-enrollment.md) for the provider-specific parameters and requirements.

