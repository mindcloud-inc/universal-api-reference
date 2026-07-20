# BlogIn: Update Member

Updates an existing member in BlogIn.

```
PUT https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/update-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlogIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/update-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "email": "ava@example.com",
  "username": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/update-member', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "email": "ava@example.com",
    "username": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The ID of the member to update. |
| `email` | string | yes | The email address of the member. |
| `username` | string | yes | The username of the member. |
| `name` | string | no | The first name of the member. |
| `surname` | string | no | The surname of the member. |
| `access_level` | string | no | The access level of the member. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_level": "string",
      "avatar": "string",
      "email": "ava@example.com",
      "id": 1,
      "job_title": "string",
      "name": "Ava Chen",
      "phone": "string",
      "status": "string",
      "surname": "Ava Chen",
      "teams": [
        {}
      ],
      "time_registered": "string",
      "timezone": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_level` | string |  |
| `avatar` | string |  |
| `email` | string |  |
| `id` | number |  |
| `job_title` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `status` | string |  |
| `surname` | string |  |
| `teams` | array<object> |  |
| `time_registered` | string |  |
| `timezone` | string |  |
| `username` | string |  |

## Native endpoint

Through the native BlogIn API, this operation is `POST /members/:id` (base URL `https://blogin.co/api/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-member.md) for the provider-specific parameters and requirements.

