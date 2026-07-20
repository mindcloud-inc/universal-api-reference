# Edusign: Create Student

Creates a new student in Edusign.

```
POST https://connect.mindcloud.co/v1/universal/edusign/latest/actions/create-student
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/create-student" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "student": {},
  "student.firstname": "Ava",
  "student.lastname": "Chen",
  "student.email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/edusign/latest/actions/create-student', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "student": {},
    "student.firstname": "Ava",
    "student.lastname": "Chen",
    "student.email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `student` | object | yes |  |
| `student.firstname` | string | yes | Student's first name |
| `student.lastname` | string | yes | Student's last name |
| `student.email` | string | yes | Student's email |
| `student.fileNumber` | string | no |  |
| `student.photo` | string | no | Student's photo |
| `student.phone` | string | no | Student's phone |
| `student.groups[]` | array<string> | no |  |
| `student.groups[]` | array<string> | no |  |
| `student.groups[]` | array<string> | no |  |
| `student.trainingName` | string | no | Student training's name |
| `student.company` | string | no | Student's company |
| `student.sendEmailCredentials` | boolean | no | boolean to know if the API sends the credentials to the mail of the student |
| `student.apiId` | string | no | Student's External Id |
| `student.apiType` | string | no | name of the connector the student if part of (if he is) |
| `student.badgeId` | string | no |  |
| `student.studentFollowerId[]` | array<string> | no |  |
| `student.studentFollowerId[]` | array<string> | no |  |
| `student.studentFollowerId[]` | array<string> | no |  |
| `student.isicId` | string | no | Student's ISIC ID |
| `student.studentCard` | object | no |  |
| `student.studentCard.birthDate` | string | no | Student's birth date |
| `student.studentCard.diploma` | string | no | Student's diploma |
| `student.studentCard.studentNationalId` | string | no | Student's national ID |
| `student.studentCard.cardExpirationDate` | string | no | Student's card expiration date |
| `student.studentCard.schoolYear` | string | no | Student's school year |
| `student.newPasswordNeeded` | boolean | no | Ask the student to change the password on first login (default: true) |
| `student.hidden` | number | no | Student's hidden status |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `student.tags[]` | array<string> | no |  |
| `student.tags[]` | array<string> | no |  |
| `student.tags[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "id": "string",
        "type": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |
| `result.id` | string |  |
| `result.type` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `POST /v1/student` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-student.md) for the provider-specific parameters and requirements.

