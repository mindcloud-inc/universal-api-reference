# Time Doctor: Invite User

Creates a new user invitation in Time Doctor.

```
POST https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/invite-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Time Doctor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/invite-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/invite-user', {
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
| `email` | string | yes | Email of the invited user. |
| `name` | string | no | Optional full name of the invited user. |
| `role` | string | no | Role of the invited user in the company. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `userId` | string |  |

## Native endpoint

Through the native Time Doctor API, this operation is `POST /api/1.1/invitations` (base URL `https://api2.timedoctor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-user.md) for the provider-specific parameters and requirements.

