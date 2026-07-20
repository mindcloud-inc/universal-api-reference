# Kameleoon: Get account



```
GET https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kameleoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-account?connectionId=$CONNECTION_ID&accountId=12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-account?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | Account identifier from Kameleoon. Example: `12345`. |

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

Through the native Kameleoon API, this operation is `GET accounts/:accountId` (base URL `https://api.kameleoon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

