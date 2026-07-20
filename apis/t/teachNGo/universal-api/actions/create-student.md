# Teach 'n Go: Create Student

Creates a new student in Teach 'n Go.

```
POST https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/create-student
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teach 'n Go `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/create-student" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fname": "Ava Chen",
  "lname": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/create-student', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fname": "Ava Chen",
    "lname": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fname` | string | yes | The student's first name. |
| `lname` | string | yes | The student's last name. |
| `emailAddress` | string | no | The student's email address. |
| `mobilePhone` | string | no | The student's mobile phone number. |
| `gender` | string | no | Male, Female, or Not specified. |
| `dateOfBirth` | date | no | The student's date of birth. |
| `registrationDate` | date | no | The date the student was registered. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Teach 'n Go API returns.

## Native endpoint

Through the native Teach 'n Go API, this operation is `POST /api/student` (base URL `https://app.teachngo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-student.md) for the provider-specific parameters and requirements.

