# AbcSubmit: Create Account

Creates a new AbcSubmit account.

```
POST https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/create-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AbcSubmit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/create-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userName": "Ava Chen",
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen",
  "password": "string",
  "confirmPassword": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/create-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userName": "Ava Chen",
    "email": "ava@example.com",
    "firstName": "Ava",
    "lastName": "Chen",
    "password": "string",
    "confirmPassword": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userName` | string | yes | The username for the new AbcSubmit account. |
| `email` | string | yes | The email address for the new AbcSubmit account. |
| `firstName` | string | yes | The first name for the new account. |
| `lastName` | string | yes | The last name for the new account. |
| `password` | string | yes | The password for the new AbcSubmit account. |
| `confirmPassword` | string | yes | Repeat the password for confirmation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native AbcSubmit API, this operation is `POST /api/v1/users/create-account` (base URL `https://www.abcsubmit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-account.md) for the provider-specific parameters and requirements.

