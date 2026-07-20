# Edusign: Update Student

Updates an existing student in Edusign.

```
PUT https://connect.mindcloud.co/v1/universal/edusign/latest/actions/update-student
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/update-student" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "student": {},
  "student.id": "string",
  "student.firstname": "Ava",
  "student.lastname": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/edusign/latest/actions/update-student', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "student": {},
    "student.id": "string",
    "student.firstname": "Ava",
    "student.lastname": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `student` | object | yes |  |
| `student.id` | string | yes | Student's ID |
| `student.firstname` | string | yes | Student's first name |
| `student.lastname` | string | yes | Student's last name |
| `student.email` | string | no | Student's email |
| `student.fileNumber` | string | no | Student's file number |
| `student.photo` | string | no | Student's photo |
| `student.hidden` | boolean | no | Student's hidden status |
| `student.groups[]` | array<string> | no |  |
| `student.groups[]` | array<string> | no |  |
| `student.groups[]` | array<string> | no |  |
| `student.phone` | string | no | Student's phone |
| `student.trainingName` | string | no | Student training's name |
| `student.company` | string | no | Student's company |
| `student.apiId` | string | no | Student's External Id |
| `student.apiType` | string | no | name of the connector the student if part of (if he is) |
| `student.badgeId` | string | no | Student's Badge Id |
| `student.studentFollowerId[]` | array<string> | no |  |
| `student.studentFollowerId[]` | array<string> | no |  |
| `student.studentFollowerId[]` | array<string> | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `student.tags[]` | array<string> | no |  |
| `student.tags[]` | array<string> | no |  |
| `student.tags[]` | array<string> | no |  |
| `student.variables[]` | array<object> | no |  |
| `student.variables[]` | array<object> | no |  |
| `student.variables[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `PATCH /v1/student/` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-student.md) for the provider-specific parameters and requirements.

