# Worksnaps: Create a new user

Creates a new user in Worksnaps.

```
POST https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/create-a-new-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worksnaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/create-a-new-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/create-a-new-user', {
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
| `body` | string | no | Raw XML request body for this Worksnaps endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "last_name": "Chen",
      "login": "string",
      "password": "string",
      "timezone_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | the email of the user |
| `first_name` | string | the first name of the user |
| `id` | number | the ID of the user |
| `last_name` | string | last name of the user |
| `login` | string | the login of the user |
| `password` | string | the password of the user |
| `timezone_id` | number | the timezone ID of the user |

## Native endpoint

Through the native Worksnaps API, this operation is `POST /users.xml` (base URL `https://api.worksnaps.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-new-user.md) for the provider-specific parameters and requirements.

