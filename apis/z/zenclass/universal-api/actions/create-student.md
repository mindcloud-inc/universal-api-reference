# Zenclass: Create student

Creates a new student profile in Zenclass.

```
POST https://connect.mindcloud.co/v1/universal/zenclass/latest/actions/create-student
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenclass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zenclass/latest/actions/create-student" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zenclass/latest/actions/create-student', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Student email address. |
| `firstName` | string | no | Student first name. |
| `lastName` | string | no | Student last name. |
| `sendEmail` | boolean | no | Whether Zenclass should email the student. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `user_id` | string | Created student UUID. |

## Native endpoint

Through the native Zenclass API, this operation is `POST /api/v1/student` (base URL `https://api.zenclass.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-student.md) for the provider-specific parameters and requirements.

