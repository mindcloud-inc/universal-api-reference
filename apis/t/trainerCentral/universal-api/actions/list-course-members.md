# TrainerCentral: List Course Members

Retrieves course members from TrainerCentral.

```
GET https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/list-course-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrainerCentral `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/list-course-members?connectionId=$CONNECTION_ID&limit=25&offset=0&courseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "courseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/list-course-members?${params}`, {
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
| `courseId` | string | yes | The TrainerCentral course ID whose learner membership list should be fetched. |
| `searchText` | string | no | Optional learner name search text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedLesson": 1,
      "completionPercentage": 1,
      "country": "string",
      "course": "string",
      "courseId": "string",
      "courseMembersId": "string",
      "email": "ava@example.com",
      "enrolledTime": 1,
      "formattedTotalRevenue": "string",
      "id": "string",
      "imageUrl": "https://example.com",
      "ipAddress": "string",
      "lastLogin": 1,
      "name": "Ava Chen",
      "orgId": "string",
      "orgMemberId": "string",
      "role": "string",
      "status": "string",
      "time": 1,
      "totalLesson": 1,
      "totalRevenue": 1,
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedLesson` | number | Number of completed lessons in the course. |
| `completionPercentage` | number | Course completion percentage. |
| `country` | string | Learner country. |
| `course` | string | Course ID. |
| `courseId` | string | Course ID. |
| `courseMembersId` | string | TrainerCentral course-member record ID. |
| `email` | string | Learner email address. |
| `enrolledTime` | number | Course enrollment time in milliseconds since epoch. |
| `formattedTotalRevenue` | string | Formatted revenue string for this learner in the course. |
| `id` | string | Course-member record ID. |
| `imageUrl` | string | Learner profile image URL. |
| `ipAddress` | string | Last known learner IP address. |
| `lastLogin` | number | Learner last login time in milliseconds since epoch. |
| `name` | string | Learner display name. |
| `orgId` | string | TrainerCentral academy org ID. |
| `orgMemberId` | string | TrainerCentral academy member ID. |
| `role` | string | TrainerCentral role code for the course member. |
| `status` | string | TrainerCentral learner-course status code. |
| `time` | number | Last update time in milliseconds since epoch. |
| `totalLesson` | number | Total number of lessons in the course. |
| `totalRevenue` | number | Total revenue for this learner in the course. |
| `userId` | string | TrainerCentral user ID. |

## Native endpoint

Through the native TrainerCentral API, this operation is `GET /course/:courseId/courseMembers.json` (base URL `{{credentials.academyUrl}}/api/v4/{{credentials.orgId}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-course-members.md) for the provider-specific parameters and requirements.

