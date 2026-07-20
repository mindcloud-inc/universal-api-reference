# Classe365: Upsert Student

Creates or updates a student in Classe365.

```
POST https://connect.mindcloud.co/v1/universal/classe365/latest/actions/upsert-student
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Classe365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/classe365/latest/actions/upsert-student" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/classe365/latest/actions/upsert-student', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `admission_number` | string | no | Student admission number. |
| `father_name` | string | no | Father name. |
| `first_name` | string | no | Student first name. |
| `gender` | string | no | Student gender. |
| `id` | string | no | Student id for updates. |
| `last_name` | string | no | Student last name. |
| `mother_name` | string | no | Mother name. |
| `parents_contact` | string | no | Parents contact number. |
| `parents_email` | string | no | Parents email. |
| `student_contact` | string | no | Student contact number. |
| `student_dob` | string | no | Student date of birth in YYYY-MM-DD. |
| `student_email` | string | no | Student email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "admissionNumber": "string",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "studentEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admissionNumber` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `studentEmail` | string |  |

## Native endpoint

Through the native Classe365 API, this operation is `POST /rest/student` (base URL `https://{{credentials.username}}.classe365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-student.md) for the provider-specific parameters and requirements.

