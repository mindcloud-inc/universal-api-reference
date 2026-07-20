# Zenclass: Update student

Updates an existing student profile in Zenclass.

```
PUT https://connect.mindcloud.co/v1/universal/zenclass/latest/actions/update-student
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenclass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zenclass/latest/actions/update-student" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zenclass/latest/actions/update-student', {
  method: 'PUT',
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
| `city` | string | no | Updated city. |
| `email` | string | yes | Existing student email address. |
| `firstName` | string | no | Updated first name. |
| `lastName` | string | no | Updated last name. |
| `newEmail` | string | no | New student email address. |
| `phone` | string | no | Updated phone number. |

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
| `user_id` | string | Updated student UUID. |

## Native endpoint

Through the native Zenclass API, this operation is `PUT /api/v1/student` (base URL `https://api.zenclass.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-student.md) for the provider-specific parameters and requirements.

