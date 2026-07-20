# TrainerCentral: Invite Learner to Course

Invites a learner to a course in TrainerCentral.

```
POST https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/invite-learner-to-course
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrainerCentral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/invite-learner-to-course" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "courseAttendee.email": "ava@example.com",
  "courseAttendee.firstName": "Ava",
  "courseAttendee.lastName": "Chen",
  "courseAttendee.courseId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/invite-learner-to-course', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "courseAttendee.email": "ava@example.com",
    "courseAttendee.firstName": "Ava",
    "courseAttendee.lastName": "Chen",
    "courseAttendee.courseId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `courseAttendee.email` | string | yes | The learner email address to invite. |
| `courseAttendee.firstName` | string | yes | The learner first name. |
| `courseAttendee.lastName` | string | yes | The learner last name. |
| `courseAttendee.courseId` | string | yes | The course ID the learner should be invited to. |
| `courseAttendee.password` | string | no | Optional learner password. |
| `courseAttendee.expiryTime` | number | no | Optional course access expiry timestamp in milliseconds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "courseMember": [
        {
          "completionPercentage": "string",
          "courseId": "string",
          "courseMembersId": "string",
          "currentStatus": "string",
          "id": "string",
          "invitedTime": "string",
          "orgId": "string",
          "orgMemberId": "string",
          "role": "string",
          "status": "string",
          "time": "string"
        }
      ],
      "portalMember": {
        "email": "ava@example.com",
        "emailId": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "invitedBy": "string",
        "lastName": "Chen",
        "lastUpdatedTime": "string",
        "links": {
          "enrolledCourses": "https://example.com",
          "enrolledSessions": "https://example.com"
        },
        "loginType": "string",
        "name": "Ava Chen",
        "orgId": "string",
        "orgMemberId": "string",
        "role": "string",
        "status": "string",
        "time": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `courseMember[].completionPercentage` | string |  |
| `courseMember[].courseId` | string |  |
| `courseMember[].courseMembersId` | string |  |
| `courseMember[].currentStatus` | string |  |
| `courseMember[].id` | string |  |
| `courseMember[].invitedTime` | string |  |
| `courseMember[].orgId` | string |  |
| `courseMember[].orgMemberId` | string |  |
| `courseMember[].role` | string |  |
| `courseMember[].status` | string |  |
| `courseMember[].time` | string |  |
| `portalMember.email` | string |  |
| `portalMember.emailId` | string |  |
| `portalMember.firstName` | string |  |
| `portalMember.id` | string |  |
| `portalMember.invitedBy` | string |  |
| `portalMember.lastName` | string |  |
| `portalMember.lastUpdatedTime` | string |  |
| `portalMember.links.enrolledCourses` | string |  |
| `portalMember.links.enrolledSessions` | string |  |
| `portalMember.loginType` | string |  |
| `portalMember.name` | string |  |
| `portalMember.orgId` | string |  |
| `portalMember.orgMemberId` | string |  |
| `portalMember.role` | string |  |
| `portalMember.status` | string |  |
| `portalMember.time` | string |  |

## Native endpoint

Through the native TrainerCentral API, this operation is `POST /addCourseAttendee.json` (base URL `{{credentials.academyUrl}}/api/v4/{{credentials.orgId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-learner-to-course.md) for the provider-specific parameters and requirements.

