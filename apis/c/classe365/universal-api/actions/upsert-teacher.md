# Classe365: Upsert Teacher

Creates or updates a teacher in Classe365.

```
POST https://connect.mindcloud.co/v1/universal/classe365/latest/actions/upsert-teacher
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Classe365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/classe365/latest/actions/upsert-teacher" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/classe365/latest/actions/upsert-teacher', {
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
| `first_name` | string | no | Teacher first name. |
| `gender` | string | no | Teacher gender. |
| `id` | string | no | Teacher id for updates. |
| `is_academic` | string | no | 1 for academic teacher. |
| `last_name` | string | no | Teacher last name. |
| `teacher_contact` | string | no | Teacher contact number. |
| `teacher_dob` | string | no | Teacher date of birth in YYYY-MM-DD. |
| `teacher_email` | string | no | Teacher email. |
| `teacher_id` | string | no | Teacher code/identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "teacherEmail": "ava@example.com",
      "teacherId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `teacherEmail` | string |  |
| `teacherId` | string |  |

## Native endpoint

Through the native Classe365 API, this operation is `POST /rest/teacher` (base URL `https://{{credentials.username}}.classe365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-teacher.md) for the provider-specific parameters and requirements.

