# Kameleoon: Update account



```
PUT https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/update-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kameleoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/update-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "12345"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/update-account', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "12345"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | Account identifier from Kameleoon. Example: `12345`. |
| `email` | string | no | Updated email for the account. |
| `firstName` | string | no | Updated first name. |
| `lastName` | string | no | Updated last name. |
| `password` | string | no | Updated password. |
| `passwordConfirm` | string | no | Password confirmation when changing password. |
| `preferredLocale` | string | no | Preferred locale: fr, en, or de. |
| `status` | string | no | Account status value. |

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

Through the native Kameleoon API, this operation is `PATCH accounts/:accountId` (base URL `https://api.kameleoon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-account.md) for the provider-specific parameters and requirements.

