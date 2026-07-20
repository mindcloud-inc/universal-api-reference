# Innform: Update User

Updates a user in Innform by ID or email.

```
PUT https://connect.mindcloud.co/v1/universal/innform/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Innform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/innform/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "idOrEmail": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/innform/latest/actions/update-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "idOrEmail": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | Updated user email. |
| `groups[]` | array<string> | no | Updated list of group names. Accepts multiple values as an array. |
| `idOrEmail` | string | yes | User UUID or email address. |
| `locale` | string | no | Updated user locale code. |
| `mobile` | string | no | Updated mobile number. |
| `name` | string | no | Updated user name. |
| `property` | string | no | Updated property name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "id": "string",
      "locale": "string",
      "mobile": "string",
      "name": "Ava Chen",
      "role": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `id` | string |  |
| `locale` | string |  |
| `mobile` | string |  |
| `name` | string |  |
| `role` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Innform API, this operation is `PUT /users/{idOrEmail}` (base URL `https://api.innform.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

