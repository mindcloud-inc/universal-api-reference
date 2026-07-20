# Kameleoon: Get all accounts



```
GET https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kameleoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-accounts?connectionId=$CONNECTION_ID&paramsIo=page%3D1%2C%20perPage%3D20" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paramsIo": "page=1, perPage=20"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-accounts?${params}`, {
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
| `paramsIo` | string | yes | Required query object documented by Kameleoon for /accounts requests. Provide URL-encoded JSON in paramsIO (example: {"page":1,"perPage":20}). Example: `page=1, perPage=20`. |

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

Through the native Kameleoon API, this operation is `GET accounts` (base URL `https://api.kameleoon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-accounts.md) for the provider-specific parameters and requirements.

