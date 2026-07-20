# Kameleoon: Create account



```
POST https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/create-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kameleoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/create-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen",
  "password": "string",
  "passwordConfirm": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/create-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "firstName": "Ava",
    "lastName": "Chen",
    "password": "string",
    "passwordConfirm": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email associated with the account. |
| `firstName` | string | yes | First name of the account user. |
| `lastName` | string | yes | Last name of the account user. |
| `password` | string | yes | Password for the account. |
| `passwordConfirm` | string | yes | Password confirmation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "isPasswordExpired": true,
      "isProductRecoAllowed": true,
      "lastName": "Chen",
      "passwordBlocked": true,
      "preferredLocale": "string",
      "roles": [
        {}
      ],
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
| `firstName` | string |  |
| `id` | number |  |
| `isPasswordExpired` | boolean |  |
| `isProductRecoAllowed` | boolean |  |
| `lastName` | string |  |
| `passwordBlocked` | boolean |  |
| `preferredLocale` | string |  |
| `roles` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native Kameleoon API, this operation is `POST accounts` (base URL `https://api.kameleoon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-account.md) for the provider-specific parameters and requirements.

