# TalentLMS: Enroll User to Course

Enrolls a user in a course in TalentLMS.

```
POST https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/enroll-user-to-course
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentLMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/enroll-user-to-course" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "courseId": 1,
  "userId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/enroll-user-to-course', {
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
| `courseId` | number | yes | Numeric course ID. |
| `userId` | number | yes | Numeric user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "role": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.role` | string |  |

## Native endpoint

Through the native TalentLMS API, this operation is `POST /enrollments` (base URL `https://{{credentials.domain}}.talentlms.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enroll-user-to-course.md) for the provider-specific parameters and requirements.

